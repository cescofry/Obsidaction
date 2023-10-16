---
publish: true
---
An action is a `blockcode` type that allows to define logic to apply to [Inputs](Inputs.md), [Bindings](Bindings.md) and [Templates](Templates.md).



```default:action
{
    appendToDailyFormat : "YYYY-MM"
}
```

> #todo 
> File strategy: `selectedFile`, `dateFormat`, `sequentialFormat`
> 
> Insert strategy: `insertAfterRegex`, `insertBeforeRegex`, where empty regex value will insert at beginning/end of file. If missing defaults to append at the end of the file.
>
