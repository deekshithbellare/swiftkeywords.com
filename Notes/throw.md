# throw

Error is thrown from from the throwing functions using `throw`. Thrown error should confirm to Error protocol.

Throw will move the control back to the calling point where error thrown should be gracefully handled.

```
fun validateUser(fistName:String?,lastName:String?) throws {
guard firstName = fistName, firstName.isEmpty else {
throw UserValidate.firstNameNotFound
}
}
```
