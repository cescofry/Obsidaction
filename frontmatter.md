---
publish: true
---

## FrontMatter

Frontmatter is used to define settings fore the [Inputs](Inputs.md) that then need to be replaced in the rest of the md file. The title for the flow as well as the [Output](Output.md) format is also defined here.

```YAML
---

title: <TITLE FOR FLOW>

inputs:

- id: <UNIQUE ID>

  textField:

    keyboardType: number

- id: <ANOTHER UNIQUE ID>
  picker:
    options:
    - Kg
    - lbs

output:
	dateFormat: “YYYY-MM-dd.md”
---
```
