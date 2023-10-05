---
publish: true
---
The body template is represented by standard markdown, that will be rendered by a native [Attributed String](https://developer.apple.com/documentation/foundation/attributedstring) in the iOS App. Every input in the frontmatter needs to be referenced by ID in the template format `{{id}}`.
A template id that is not found in frontmatter will cause an error during flow creation.
Every input replacement will be rendered in a new line. 
> Because markdown does not support input types every input template will be replaced by a native SwiftUI view and inserted in between the markdown views. 

If a `<style></style>` section is found it will be used to further style the native [Attributed String](<[Attributed String](https://developer.apple.com/documentation/foundation/attributedstring)>).




```md
# Weight

{{weight}}

# Unit

{{unit}}

> Try to record your weight every day around the same time.

<style>
h1 {
	color: green;
	text-align: left;
}
</style>
```


