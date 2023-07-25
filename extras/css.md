# CSS

## Question nodes

This works with the stock question nodes that ship with the extension, so it looks like this:

![](<../.gitbook/assets/image (3).png>)

Feel free to modify!

```css
/* change font color and weight */
span[data-link-title^="[[QUE]] - "] > span {
  font-weight: 500; 
  color: #99890E !important; 
}

/* add icon before page ref */
span[data-link-title^="[[QUE]] - "]:before {
    content: '🔎  ' 
}

/* color the QUE complex page ref */
span[data-link-title="QUE"] > span {
  font-weight: 500; 
  color: #99890E !important; 
}
```

## Claim nodes

This works with the stock claim nodes that ship with the extension. Feel free to modify!

```css
span[data-link-title^="[[CLM]]"] > span {
   color: #7DA13E; !important;
   font-weight: 500;
}

span[data-link-title^="[[CLM]] "]:before {
    content: '🌲 ' 
}
```

## Evidence nodes

This works with the stock claim nodes that ship with the extension. Feel free to modify!

```css
span[data-link-title^="[[EVD]] - "] > span {
   /* color: var(--cl-black) !important; */
   color: #DB134A !important;
}

span[data-link-title^="[[EVD]] - "]:before {
    content: '🌱  '
}
```



## Source nodes

This works with the stock source nodes that ship with the extension. Feel free to modify!

```css
span[data-link-title^="@"] > span {
   color: #9E9E9E;
}

span[data-link-title^="@"]:before {
    content: '🗒️ ' 
}
```
