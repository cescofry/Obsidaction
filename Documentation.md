---
publish: true
---

## FrontMatter

Example of Frontmatter
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
---
```


# Inputs
Description of all supported inputs

## textField

```YAML
- id: <UNIQUE ID>

  textField:
    keyboardType: number
    lineLimit: 3
```

#### Options

**keyboardType** : what kind of keyboard should textfield being associated with. **Values**: `default`, `number`, `email` 

**lineLimit** : how many lines are shown. This will switch from textField to textArea for any value greater than 1

---

## toggle

```YAML
- id: <UNIQUE ID>

  toggle:

    defaultOn: true
```

#### Options

**defaultOn** : defaults the toggle to On

---

## picker

```YAML
- id: <UNIQUE ID>

  picker:
    deafultsTo: Kg
    style: dropDown
    options:
    - Kg
    - lbs
```

#### Options

**defaultTo** : (*optional*) pre select one of the option values
**style** : which picker style to show. **Values**: `dropDown` , `segmented` 

---

## stepper

```YAML
- id: <UNIQUE ID>

  stepper:
   lowerBound: 0
   upperBound: 100
   step: 2
   startValue: 10
   previewStyle: number
```

#### Options

**lowerBound** : smaller value the stepper will reached

**upperBound** : higher value the stepper will reached

**step** :  every step will increase or decrease by this value

**startValue** :  the starting value

**previewStyle** :  the style representing the preview of the current value. **Values** : number, progress


---

# Output
- [ ] Output #todo 

```YAML
	output:
		dateFormatToFolder: “YYYY-MM-dd”
		insertAfterRegex

```

Output needs to define in which file and in which position in the file to save.

File strategy: `selectFile`, `dateFormatToFolder`, `sequentialFormatToFolder`

Insert strategy: `insertAfterRegex`, `insertBeforeRegex`, nil regex will insert at beginning/end of file.

