# Playground

We have an experimental visual space for interacting with your discourse graph, called the **Playground**. It's experimental because we aren't quite sure about the core use cases: if you use it and find it useful, we'd love to hear from you!

Here is what the interface looks like:

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.28.08@2x.png>)

You can toggle whether the playground is fullscreen by clicking on the maximize/minimize icon in the top right portion of the menubar.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.29.55.gif>)

You can pan (by click-dragging) and zoom (w/ mouse wheel) the canvas.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.51.56.gif>)

You can call up the Roam sidebar or [query drawer](../../guides/querying-your-discourse-graph.md) while the playground is maximized. You can insert results into the canvas from the query drawer by ctrl+clicking on individual results.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 12.16.41.gif>)

### Node function modes

In the top left are node function modes that you can switch between.&#x20;

**Normal**: in this mode, you can create new nodes on the playground by clicking on an empty space, or select and move nodes.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.33.30.gif>)

You can also activate this mode with the hotkey combination `CMD+n` (Mac) or `CTRL+n` (windows)

**Draw edge:** In this mode, you can draw edges between nodes. When this mode is activated, simply click on the node you want to be the _source_, then click on the node you want to be the _target_. You can then click on the label for the edge to select the relation you want.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.36.16 (1).gif>)

You can also activate this mode with the hotkey combination `CMD+c` (Mac) or `CTRL+c` (windows)

**Edit:** In this mode, you can edit the text of nodes. Clicking on a node will bring up an editing window where you can edit the text.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.38.42.gif>)

You can also activate this mode with the hotkey combination `CMD+e` (Mac) or `CTRL+e` (windows)

**Delete:** In this mode, you can delete nodes by clicking on them.&#x20;

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.40.33.gif>)

You can also activate this mode with the hotkey combination `CMD+d` (Mac) or `CTRL+d` (windows)

**Alias:** In this mode, you can create aliases for nodes, handy if you have very long nodes that you want to see by a shorthand in this playground. Clicking on the node calls up the editing window where you can define an alias for a node. Remove an alias by deleting all text in the editing window.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.42.14.gif>)

You can also activate this mode with the hotkey combination `CMD+a` (Mac) or `CTRL+a` (windows)

### **Canvas functions**

In the top right corner, there are a number of functions you can access for the canvas.

The **node picker** allows you to control, in normal mode, what type of node you create when you create a new node.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.44.05.gif>)

The **filter** allows you to filter what node or edge types to show on the canvas (they won't be removed when filtered out, just hidden).

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.47.33.gif>)

The **search** function allows you to search for and jump to nodes on the canvas by text.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.49.32.gif>)

The **minimap** opens up a minimap on the bottom right that you can use to navigate a large canvas.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.52.45.gif>)

The **overlay** toggles whether nodes on the canvas have the [discourse-context-overlay.md](../../guides/exploring-your-discourse-graph/discourse-context-overlay.md "mention") on them.

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 11.54.38.gif>)

**Draw existing edges** automatically draws any existing edges between nodes on the canvas (currently broken).

**Generate Roam blocks** creates a page that contains the nodes on the canvas, in block formats that instantiate any existing relation patterns between nodes on the canvas. The page name will be of the form `Auto generated from <playgroundPageName>`

![](<../../.gitbook/assets/CleanShot 2022-08-10 at 12.01.13.gif>)

**Export** calls up an export dialog that you can use to [export the nodes to csv/json/markdown](../../guides/sharing-your-discourse-graph.md).

### Use cases

This is still in experimentation, but some possible use cases include:

* **Early stage sensemaking**: after creating a set of evidence and claim notes from reading, go to the Playground to make sense of how they relate to each other, by opening up the query drawer to call up these evidence/claim notes and inserting them into the canvas.
* **Gathering items for export**: use the query drawer to collect subsets of your discourse graph and then export for sharing.
