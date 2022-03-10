# Creating discourse nodes

The extension makes it easy to factor parts of your notes into formal of a discourse graph (claims, evidence, etc.).&#x20;

Simply select the text you want to turn into a formal discourse graph node (e.g., QUE, CLM, EVD), then press hotkey (default is `\`, but you can edit this in the extension config page) to open up the refactor menu, and press appropriate shortcut key (e.g., E for evidence); system will create new page with the text as title and appropriate metadata and boilerplate sections.

Demo:

{% embed url="https://www.loom.com/share/471fcf7dc13246439cb35feedb110470" %}

You can customize templates for nodes in the config page for the node. It is in the name space `discourse-graph/nodes/NameOfNode`. For example, here is the config page for the stock evidence node, and its template:

![](<../.gitbook/assets/CleanShot 2022-03-09 at 23.40.33.png>)
