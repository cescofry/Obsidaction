---
publish: true
---


Inputs are the most important feature of Obsidaction. Inputs use a list-like syntax to represent elements that can be interacted with when rendered in the app.
A canonical input will look like this `- [id:type:value] description` 
- `id` is a unique identifier for the input. It will be used by the [Body template](Body%20template.md) and by [Bindings](Bindings.md) to reference the value of the input.
- `type` the type of the input that needs to be represented. each inout type is listed in this page, but some of them can be inferred. Read more in the list below.
- `value` is an optional value that is assigned as default. For example a picker may decide to have one of its options pre-selected.
- `description` everything after the `[]` is considered a description and will be placed, where possible, beside the input when rendered.

## textField

```
- [id:number:value] description
```

```
- [id] description
```

#### Options
**value**: (*optional*)starting value
**type** :  the type is used to either define the keyboard type (`number`, `email`) or if this is a `textField`or a `textArea`
**description**: (*optional*) placeholder hint that shows on an empty value. 
> An input with only the `id` defined will default to a `textField` with a standard keyboard. 
---

## toggle

```
- [id:true] description
```

#### Options
**value**: A toggle is defined by its value, differently from other inputs, it does not specify it's type. Instead if the value represents a boolean (`true`, `false`, `on`, `off`, `yes`, `no`) it will be rendered as a toggle
**description**: (*optional*) This will be rendered before the toggle.

---

## picker

```
- [id:segmented:option 1/option 2:option 2] description
```

```
- [id:option 1/option 2] description
```



#### Options

**value** : (*optional*) pre select one of the option values
**style** : which picker style to show. **Values**: `dropDown` , `segmented` 
**options**: a `/` separated list of the options that can be selected.
**description**: (*optional*) placeholder hint that shows on an empty value. 
#todo multiple selection.

---

## date and time picker

```
- [id:@time] description
```

```
- [id:@date] description
```


#### Options

**value** : not supported
**style** : which picker style to show. **Values**: `@time` , `@date` 
**options**: not suported
**description**: (*optional*) placeholder hint that shows on an empty value. 

---


## stepper
#todo  This component has not been implemented yet.

```
- [id:stepper:0-2-100:10] description
```

#### Options
**type** :  `stepper`
**range** : defines the range with a `lowerBound-stepValue-upperBound` syntax where `lowerBound` and `upperBound` are the limit of the stepper and `stepValue` is the step the value makes when the `+/-` buttons are tapped.
**value** :  (*optional*) the starting value. `lowerBound`is used if missing.

## Timer
#todo  This component has not been implemented yet.

```
- [id:timer:600] description
```

#### Options
**type** :  `timer`
**value** :  the starting value for the timer. 



# Inputs and SwiftUI

Inputs are represented in the App using [SwiftUI](https://developer.apple.com/xcode/swiftui/). 
There is currently minimal support for [Markdown](https://www.hackingwithswift.com/quick-start/swiftui/how-to-render-markdown-content-in-text) in SwiftUI.
Inputs are only distant cousins of Markdown, and they are parsed and represented by the app. Only the inputs listed in this page are currently supported. 
That doesn't mean new inputs should not be added. If you think a new input type should be develop please file an [issue](https://github.com/cescofry/Obsidaction/issues) including the format of markdown for the input `id:type:options:value` and the SwiftUI code to represent it (or alternatively a description of what the UI should look like).
