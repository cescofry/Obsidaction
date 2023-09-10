---
publish: true
---
All the inputs for each template are found in the [frontmatter](frontmatter.md) inside the input key. The `id` has to be unique for the file and also referenced as a replaceable in the [Body template](Body%20template.md).

## textField

```YAML
- id: <UNIQUE ID>

  textField:
    value: “”
    placeholder: “”
    keyboardType: number
    lineLimit: 3
```

#### Options
**value**: (*optional*)starting value
**placeholder**: (*optional*) placeholder hint that shows on an empty value. 

**keyboardType** : (*optional*) what kind of keyboard should textfield being associated with. **Values**: `default`, `number`, `email` 

**lineLimit** : (*optional*) how many lines are shown. This will switch from textField to textArea for any value greater than 1

---

## toggle

```YAML
- id: <UNIQUE ID>

  toggle:

    value: true
```

#### Options

**value** : defaults the toggle to On. False if omitted. 

---

## picker

```YAML
- id: <UNIQUE ID>

  picker:
    value: Kg
    style: dropDown
    options:
    - Kg
    - lbs
```

#### Options

**value** : (*optional*) pre select one of the option values
**style** : which picker style to show. **Values**: `dropDown` , `segmented` 
**options**: the options that can be selected. 
#todo multiple selection.

---

## stepper

```YAML
- id: <UNIQUE ID>

  stepper:
   lowerBound: 0
   upperBound: 100
   step: 2
   value: 10
   previewStyle: number
```

#### Options

**lowerBound** : smaller value the stepper will reached

**upperBound** : higher value the stepper will reached

**step** :  every step will increase or decrease by this value

**value** :  the starting value

**previewStyle** :  the style representing the preview of the current value. **Values** : `number`, `progress`
