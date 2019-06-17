## Composition over inheritance 

```kotlin
abstract class Automobile {
    abstract fun drive()
    abstract fun fly()
}
class Twingo : Automobile() {
    override fun drive() = println("I can do that")
    override fun fly() = println("Sorry I can't")
}
```
