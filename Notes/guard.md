# guard

guard statement is a conditional statement where an expression needs to be true for the continuation of execution. If expression is false, mandatory else block is executed and control is moved out of the current scope.

guard statement needs to be of type Bool or it should be optional chaining

```
extension File { 
internal func write<S: StringProtocol>(_ string: S) -> Bool{ 
guard string != contents else { return false} 
guard let path = path else { return false} 
guard let stringData = String(string).data(using: .utf8) else { return false } 
//Write data
}
```

write method inside File class, perfoms write operation after perfoming all required validations. If any of the condition fails, control is moved out of the function using return statement.