---
publish: true
---

# Weight tracking

- [weight:number] Enter your Weight
- [unit:segmented:kg/lb] Unit

```converted_weight:binding

const defaultUnit = 'kg';
const kgToLb = 2.204;
if (context.unit == defaultUnit) {
	return context.weight;
} else if (context.unit == 'kg') {
	return '' + (context.weight_Int * kgToLb);
} else {
	return '' + (context.weight_Int / kgToLb);
}
```

```result:template
weight:: {{converted_weight}}
```

```default:action
{
    appendToDailyFormat : "YYYY-MM-DD"
}
```
