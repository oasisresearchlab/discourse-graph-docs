# 👷♀ Installation

First create a **block** with the text `{{[[roam/js]]}}` on any page in your Roam DB. Then, create a single child of this block and type three backticks. A code block should appear. Copy this code and paste it into the child code block in your graph:

```javascript
var existing = document.getElementById("roamjs-discourse-graph-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/discourse-graph/main.js";
  extension.id = "roamjs-discourse-graph-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```

Finally, click **"Yes, I Know What I'm Doing".**

You'll know installation is successful if you can go to the page `roam/js/discourse-graph`, and see this:

![](<.gitbook/assets/CleanShot 2022-03-10 at 01.28.15.png>)

