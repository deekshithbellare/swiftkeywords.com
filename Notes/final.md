# final

Any method, property and subscripts can be prevented from overriding by using final modifier. 

Any class can be prevented from subclassing by marking it as final.

Use final when you know that a declaration does not need to be overridden. Using final makes compiler use static dispatch instead of dynamic dispatch.

```
final class Review {
var message:String
var rating:Rating
var author:Author
}
```