# Function

## Function Parameters

Swift must add parameter name when calling function, exception \_ is added in the function definition.

Kotlin is optional to add parameter name, and use =, not : 

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
fun multipleOf(number: Int, multiplier: Int = 1): Int {
    return number * multiplier
}

multipleOf(5, 8)
multipleOf(number=5, multiplier=8)
```
{% endtab %}

{% tab title="Swift" %}
```swift
func multiple(number: Int, andValue: Int = 1) -> Int {
    return number * andValue
}

multiple(number: 5, andValue: 8)

func multiple(_ number: Int, by value: Int) -> Int {
    return number * value
}
multiple(5, by: 8)
```
{% endtab %}
{% endtabs %}

#### Pass by Value

The value passed in function is value, not variable, so it cannot be changed within the function.

In Kotlin, we can add a new local variable, and set the its value to the parameter.

In Swift, we add keyword inout to indicate that the parameter is **copy-in copy-out.** And when calling the function, add **&** before the argument

```swift
func incrementAndPrint(_ value: inout Int) {
    value += 1
    print(value)
}

var value = 5
incrementAndPrint(&value)
print(value)
// 6 6
```

## Function as variables

Kotlin needs **method reference operator, ::**

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
fun add(a: Int, b: Int): Int {
    return a + b
}
var operate = ::add
operate (1, 2)
// 3
```
{% endtab %}

{% tab title="Swift" %}
```swift
func add(_ a: Int, _ b: Int) -> Int {
    return a + b
}
var operate = add
operate(1, 2)
// 3
```
{% endtab %}
{% endtabs %}



