---
publish: true
---
The output is part of the [frontmatter](frontmatter.md) yaml and defines in which file and in which position in the file to save the processed [Output](Output.md). 

```YAML
	output:
		dateFormat: “YYYY-MM-dd.md”
		insertAfterRegex

```

File strategy: `selectedFile`, `dateFormat`, `sequentialFormat`

Insert strategy: `insertAfterRegex`, `insertBeforeRegex`, where empty regex value will insert at beginning/end of file. If missing defaults to append at the end of the file. 



# Output Template
#todo COMPLETE THIS SECTION
The Output Template is used to compose the output using the values of the inputs in the native view. If the `dateFormat` or `sequentialFormat` are used a NEWFILE template could be provided to differentiate between appending to an existing file or creating a new file

```md
<!--CREATE-->
---
weight_track: true
---

<!--APPEND-->
weight:: {{weight}}
unit:: {{unit}}

```

Alternative:

<!--OUTPUT-->
```create
—-
test: true
—-
```

```append
Weight: {{weight }}
```
