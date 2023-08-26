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

output:

  appendToDailyFormat: dd-MM-yyyy

---
```


# Inputs
Description of all supported inputs

## textField

```YAML
- id: <UNIQUE ID>

  textField:

    keyboardType: number
```

#### Options

**keyboardType** : what kind of keyboard should textfield being associated with. **Values**: `default`, `number`, `email` 

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

