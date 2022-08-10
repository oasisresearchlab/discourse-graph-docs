# Querying your discourse graph

{% hint style="info" %}
**Note: a lot of the querying functionality overlaps with the RoamJS query-builder extension, which was spun off from this extension. You might find the documentation for the query-builder helpful for learning how to run queries:** [**https://roamjs.com/extensions/query-builder**](https://roamjs.com/extensions/query-builder)****
{% endhint %}

The query drawer component allows you to construct structured queries over your discourse graph, based on discourse relations (e.g., "find all evidence that supports/opposes a claim"), and reason over the results in a structured, tabular format (e.g., "find all evidence that supports a claim, and allow me to filter/sort by methodological details").&#x20;

## Quick demo

{% embed url="https://www.loom.com/share/0a9f890126944d038d12f499d4dedcbf" %}
Demo of query drawer (\*slightly\* different version from latest version, so some details of the results table are different)
{% endembed %}

## Making a query

Use Command Palette (⌘+`P` on Mac,`CTRL`+ `P` otherwise) to access the query drawer.

![](<../.gitbook/assets/CleanShot 2022-04-01 at 21.40.17.png>)

A query drawer component will open from the left. From there, you can construct structured queries of your discourse graph and explore their results in a tabular format.

![](<../.gitbook/assets/CleanShot 2022-04-01 at 21.41.02@2x.png>)

## Some common queries

### Find all evidence that informs a question

Example query:

![](<../.gitbook/assets/CleanShot 2022-04-01 at 23.47.35@2x.png>)

The results:

![](<../.gitbook/assets/CleanShot 2022-04-01 at 23.47.58@2x.png>)

### Find all evidence that supports a claim

Example query:

![](<../.gitbook/assets/CleanShot 2022-04-01 at 23.52.11@2x.png>)

The results:

![M](<../.gitbook/assets/CleanShot 2022-04-01 at 23.51.39@2x.png>)

## More advanced queries

### Mix discourse and Roam queries

Example: find all evidence that informs a question, but only if it was collected in a specific location (this example assumes at least some evidence pages have an attribute `Location::` in them)

![](<../.gitbook/assets/CleanShot 2022-04-01 at 23.57.43@2x.png>)

Results:

![](<../.gitbook/assets/CleanShot 2022-04-01 at 23.58.22@2x.png>)

### Select node attributes to display as attributes of results

Example: find all evidence that informs a question, and select a methods attribute to display so we can sort/filter on it (this example assumes at least some evidence pages have an attribute `testingRegime::` in them)

![](<../.gitbook/assets/CleanShot 2022-04-02 at 00.01.04@2x.png>)

Results (note: will display "blank" for nodes that lack values for the selected attribute):

![](<../.gitbook/assets/CleanShot 2022-04-02 at 00.01.22@2x.png>)

### Select discourse attributes to display as attributes of results

If you have defined [discourse-attributes.md](exploring-your-discourse-graph/discourse-attributes.md "mention") for the node you want to query, you can select it as a column in your query. The syntax for accessing a node's discourse attribute as a select is`discourse:discourseAttributeName`.

Example: find all claims and display their "Evidence" discourse attributes (number of supporting evidence relations) as a column.&#x20;

![](<../.gitbook/assets/CleanShot 2022-08-10 at 09.33.43@2x.png>)

Results:

![](<../.gitbook/assets/CleanShot 2022-08-10 at 09.34.36@2x.png>)

## Sorting/filtering a query's results

You can filter and sort each column in the results table.

{% file src="../.gitbook/assets/sorting-filtering-query-results.gif" %}

## Naming a query

You can name a query if you like!

![](../.gitbook/assets/rename-query.gif)

## Saving a query to its own page

You can save a query to its own page if you want to keep it around for easier access.&#x20;

![](<../.gitbook/assets/CleanShot 2022-04-02 at 00.14.15@2x.png>)

It will be saved to the namespace `discourse-graph/queries/`

![](<../.gitbook/assets/CleanShot 2022-04-02 at 00.16.26@2x.png>)
