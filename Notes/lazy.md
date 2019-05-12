# lazy

lazy stored property is a property whoose value is not calcualted until it is first accessed. A property can be marked lazy when it's value depends on other stored properties whoose value is available only after the initialisation of the entity.

A property can also be marked as lazy when initial computation is expensive, which is accessed under certain conditions only.

```
class BluePrintInteractor {
var provider: Networking! 
lazy var pinger: APIPingManager = {
return APIPingManager(provider: self.provider) }
}
```