---
publish: true
type: append_daily
trigger: send_form
action: template
---


# Fill the Form below


```obsidaction
{type: textfield, id: “name”, value: “placeholder”, keyboardType: "alphaNumeric"}
```


> [!NOTE] Name
> Enter your full name. this is used to track who created this entry


```obsidaction
{type: textfield, id: “age”, value: “placeholder”, keyboardType: "numeric"}
```


> [!NOTE] Age
> Enter your Age. This is to prove you can access all the content

```obsidaction
{type: slider, id: “weight”, value: “0”, range: [0, 300]}
```


```obsidaction
{type: button, value: “save”, action: “send_form”}
```

```obsidaction
{type: end_form}
```

# Result Document

> This is the document that gets generated from the above form.

name:: {{name}}
age:: {{age}}
weight: {{weight}}
