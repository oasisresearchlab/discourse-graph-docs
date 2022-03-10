# Nodes



* `discourse node`
  * as defined in your grammar (e.g., base grammar will include CLM or EVD, for example)
* `block`
* `page`

{% hint style="danger" %}
It is not possible to directly specify that a source or target node in a relation pattern is a `block` or `page`. These are variables that are defined implicitly at the moment, by what incoming and/or outgoing relations it connects to.&#x20;

For example, if a node's incoming relation is `references`, that implies it is a page. Similarly, if the node's incoming relation is `has child` or `has ancestor`, that implies the node is a block.&#x20;

When in doubt, check the preview of your relation pattern to ensure you're correctly expressing your intentions!
{% endhint %}
