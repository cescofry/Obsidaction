---
publish: true
---
#TODO

Sometimes [Templates](Templates.md) are not enough to express complex behaviors. Bindings are used to transform inputs into other inputs using `javascript` code.

**Example**:
```binding:id
return context.any_id == "test" ? "this is a test" : "not a test";
```

The body of the binding contains a `context` object, which contains every other input and bindings. All inputs are expressed as Strings, but context will automatically add extensions of more natural values. For example a toggle of id `is_on` will have a boolean context `context.is_on_Bool`.

The `return` keyword can be omitted for single line statements.

Since bindings can call each other, the user needs to be careful not to create infinite recursions by having binding calling each other.


