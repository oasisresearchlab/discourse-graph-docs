# Discourse attributes

You can define discourse attributes that for each discourse node, which compute a numerical "score" for each instance of the node based on its discourse relations to other nodes. In the extension, we call these **discourse attributes**.&#x20;

These attributes can be handy for sorting/querying nodes. For instance, if you create a discourse attribute for Claim nodes that is a function of the number of Evidence nodes that Support the Claim, like this:

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 09.10.10@2x.png>)

You can add discourse attributes as a column to display and sort/filter by when [querying-your-discourse-graph.md](../querying-your-discourse-graph.md "mention"). For example, in the index for Claims, you can return the Evidence attribute as a column (Select), and then sort in descending order by that attribute.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 09.29.43@2x.png>)

You can also select one of the attributes to be displayed in the [discourse-context-overlay.md](discourse-context-overlay.md "mention") by (re)naming the attribute to "Overlay".&#x20;

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 09.09.19@2x.png>)

Note: unfortunately atm you cannot edit the name of the attribute in the UI after you create it, but you can edit it by going down to the block tree on the page where the data is stored, and editing the block. Do this with some caution!

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 09.12.25.gif>)

### Basic discourse relation functions

A discourse attribute consists of one or more **discourse functions**, joined by one or more math operations. You can think of the discourse functions as variables that get their value from some discourse relations the node participates in.&#x20;

Here is the template for each discourse function: `{count:relationName:targetType}`

* `count` is the operation. Atm, this is the only supported operation for basic discourse functions. We also have experimental discourse functions that operate over the discourse attributes of related nodes (see below), which allow for other operations such as `sum` and `average`
* `relationName` is the name of the relation you want to use for the function, such as `Supported By` or `Informed By`
* `targetType` is the name of the type of target of the relation you want to use for the function (since nodes can have relationships of the same name with multiple other nodes, such as `Supported By:Claim` or `Supported By:Evidence`)

Here are some examples:

* `{count:Supported By:Evidence}`
* `{count:Informed By:Source}`
* `{count:Opposed By:Claim}`

You can use basic math operations to combine multiple discourse functions. For example, you might want to combine information across the supporting and opposing relationships to gauge how "robust" a Claim is, and give different weights to support from evidence vs. claims. You could express it like this:

`{count:Supported By:Evidence} + {count:Supported By:Claim}*0.5 - {count:Opposed By:Evidence} - {count:Opposed By:Claim}*0.5`

This function sums up the number of supporting relations and subtracts the number of opposing relations, but gives only half weight (`*0.5`) to supporting/opposing relations from Claims.

### `Compound discourse functions`

We have an experimental feature that allows us to access discourse attributes from related nodes to compute a discourse attribute. This allows us to experiment with more sophisticated ways to reason over our discourse nodes.

For example, if a Claim that only gets direct support from other Claims (e.g., because it is quite general), we might care to distinguish if its supporting Claims are themselves also supported by Evidence.

If each Claim node has a discourse attribute called Evidence that looks like this:

`{count:Supported By:Evidence} - {count:Opposed By:Evidence}`

We can define a compound discourse function that _averages_ over the Evidence attribute of Claims that support the Claim. Like this:

`{average:Supported By:Claim:Evidence}`

The syntax for these compound discourse functions is:

`{operation:relationName:targetType:targetDiscourseAttribute}`

This generalizes the syntax for the basic discourse functions by adding a discourse attribute to access from the targets, and the option of using additional operations than `count` (for now, we only support `sum` and `average`) for the function.

{% hint style="danger" %}
Note: due to Roam's API limitations, if you have a large graph, computing these compound attributes can get quite expensive, so you may experience slowness in performance, especially if you also use these attributes in the [discourse-context-overlay.md](discourse-context-overlay.md "mention"). Hopefully when Roam releases their backend API we can make this more performant!
{% endhint %}
