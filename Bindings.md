---
publish: true
---
#TODO

Sometimes the actions we want to perform on our flows are not as simple as replacing an input into a [Body template](Body%20template.md).
To achieve more complex behaviors we can use bindings. Bindings are javascript body functions that map inputs into other inputs

```binding:id
return "some js code " + other_id;
```



### Example
Let's say we want to add an additional string to the [Body template](Body%20template.md) only if the weight entered is over 100 kg.
```binding:weight_alert
weight.int > 100 : "!ALERT: overweight" : ""
```

