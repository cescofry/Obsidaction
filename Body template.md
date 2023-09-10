---
publish: true
---
The body template is represented by standard markdown, that will be rendered by a native Attributed String in the iOS App. Every input in the frontmatter needs to be referenced by ID in the template format `{{id}}`.
A template id that is not found in frontmatter will cause an error during flow creation.
Every input replacement will be rendered in a new line. 
> Because markdown does not support input types every input template will be replaced by a native SwiftUI view and inserted in between the markdown views. 


```
# Weight

{{weight}}

# Unit

{{unit}}

> Try to record your weight every day around the same time.
```
