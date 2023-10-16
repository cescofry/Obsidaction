---
publish: true
---

# Task Tracking

- [type:segmented:task/note:task]
- [tag:obsidaction/uber/hut/steamdeck]
- [task:textArea] Enter a task or a note
```text:binding
const text = context.type === 'task' ? '- [ ] ' + context.task : '- ' + context.task
const tag = context.tag !== '' ? ' #' + context.tag : ''
return text + tag
```

```result:template
{{text}}
```

```default:action
{
    appendToDailyFormat : "YYYY-MM"
}
```
