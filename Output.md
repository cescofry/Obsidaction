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

Insert strategy: `insertAfterRegex`, `insertBeforeRegex`, where empty regex value will insert at beginning/end of file. If missing defaults to insert at end of file. 
