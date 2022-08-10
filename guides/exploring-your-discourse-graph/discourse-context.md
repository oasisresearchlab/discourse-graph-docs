# Discourse context

The discourse context component adds a "higher-signal" linked references section to each discourse node, that allows you to explore _discourse_ relations (e.g., inform, support, etc.) between this node and other nodes in your discourse graph.

Things you can do:

### Group by target node

![](<../../.gitbook/assets/d-context group by.gif>)

### Filter results

![](<../../.gitbook/assets/filter results.gif>)

### Show the context of each relation

You can view the context of a relation pattern (i.e., where in your graph the extension recognized the relation) by naming one of the nodes in your relation pattern "Context". Specifying this will add a column called "Context" to the discourse context component, allowing you to view the block tree where this relation was recognized.

For example, in the following pattern for the Evidence-Supports-Claim relation, we can name the block that references the Evidence node as "Context":

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 10.32.10@2x.png>)

This allows us to view that block and its context whenever we look at Evidence-Supports-Claim relations in the discourse context, like this:

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 10.33.30.gif>)

### Demo

{% embed url="https://www.loom.com/share/0c66e95d0c71426e8090a8bc1cbf8544" %}
