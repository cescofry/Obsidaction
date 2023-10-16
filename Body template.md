---
publish: true
---
The body template is represented by standard markdown, that will be rendered by a native [Attributed String](https://developer.apple.com/documentation/foundation/attributedstring) in the iOS App.
Every [Inputs](Inputs.md) replacement will be rendered in a new line. 
> Because markdown does not support input types every input template will be replaced by a native SwiftUI view and inserted in between the markdown views. 

If a `<style></style>` section is found it will be used to further style the native [Attributed String](<[Attributed String](https://developer.apple.com/documentation/foundation/attributedstring)>).
#todo 




```md
# Weight

- [weight]

# Unit

- [unit:segmented:kg/lb]

> Try to record your weight every day around the same time.

<style>
h1 {
	color: green;
	text-align: left;
}
</style>
```


