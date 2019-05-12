# nonmutating

nonmutating setter does not modify the state of the containing instance. It changes global state. nonmutating settter is used only on structs and enumerations.

```
extension Socket {
public var sendBufferSize: Int { 
get { return getsock(opt: .sendBufferSize) 
} 
nonmutating set { setsock(opt: .sendBufferSize, value: newValue) } 
}
}
```