# mutating

`mutating` is used to mutate the property of value types. Structures and enumerations are value types. Any changes to its properties is not allowed by default, unless explicitly stated. We mutate a value type inside a function using mutating modifier.

```
struct Bool {
public mutating func toggle() { 
self = !self 
}
}
```