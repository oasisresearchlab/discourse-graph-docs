# Discourse context overlay

The discourse context overlay adds an icon next to each discourse node wherever it is referenced. This icon includes a count of the total number of discourse relations for that node (the number on the left) as well as a count of the total number of references to that node in the graph.&#x20;

![](<../../.gitbook/assets/CleanShot 2022-03-09 at 23.33.15.png>)

These counts provide a rough sense of how "robust" a given node is (discourse relations are more structured, high-signal relationshisp) relative to how "important" it is (raw references are often noisy).

Clicking on the icon brings up the [discourse context](discourse-context.md) component in-line for quick reference.

Demo:

{% embed url="https://www.loom.com/share/b3d6094cd14a466081b8aa8495eb6542" %}

This is an optional feature that is turned off by default. To turn it on, go to the grammar tab in the config page and check the box for overlay.

![](<../../.gitbook/assets/CleanShot 2022-03-09 at 23.31.22.png>)
