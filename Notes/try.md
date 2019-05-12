# try

A throwing function is called using try. It indicates that a method is being called which can throw error. try is written inside a do-catch block.

try? is used to convert error into optional value. So when error occurs, try? sends nil to the receiver. try! is used when it is known that error won't occur. try? and try! works without do-catch.

```
do {
try validateUser(firstName:"Deekshith",lastName:"Bellare) 
} catch {
}
```
