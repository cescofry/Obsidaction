---
publish: true
---

```YAML
	output:
		dateFormat: “YYYY-MM-dd.md”
		insertAfterRegex

```

Output needs to define in which file and in which position in the file to save.

File strategy: `selectedFile`, `dateFormat`, `sequentialFormat`

Insert strategy: `insertAfterRegex`, `insertBeforeRegex`, where empty regex value will insert at beginning/end of file. If missing defaults to insert at end of file. 
