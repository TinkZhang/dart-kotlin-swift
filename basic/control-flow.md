# Control Flow

## Boolean

The Boolean type is **Boolean** for Kotlin, and **Bool** for Swift.

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
var isAlive: Boolean = true
var isOld: Boolean = false
```
{% endtab %}

{% tab title="Swift" %}
```swift
var isAlive: Bool = true
var isOld: Bool = false
```
{% endtab %}
{% endtabs %}

## If

You can use if in the same way for both language, the difference is that Swift do not use \(\) in condition.

{% tabs %}
{% tab title="Koltin" %}
```swift
if (a < 0) {
    println("Negative")
} else if (a > 0) {
    println("Positive")
} else {
    println("Zero")
}
```
{% endtab %}

{% tab title="Swift" %}
```swift
if a < 0 {
    println("Negative")
} else if a > 0 {
    println("Positive")
} else {
    println("Zero")
}
```
{% endtab %}
{% endtabs %}

**If expression** for Kotlin. **If statement** for Swift, which means you can assign the if expression to a variant, and the value is the last expression if if block

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
var status = if (a < 0) {
    "Negative"
} else if( a > 0) {
    "Positive"
} else {
    "Zero"
}
```
{% endtab %}
{% endtabs %}

### Ternary Conditional Operator

Kotlin has no ternary operator.

{% tabs %}
{% tab title="Swift" %}
```swift
<CONDITION>? <TRUE VALUE>: <FALSE VALUE>
let min = a < b? a : b
```
{% endtab %}
{% endtabs %}

### While Loop

Differences

* \(\) for condition
* do-while for Kotlin and repeat-while for Swift 

{% tabs %}
{% tab title="Koltin" %}
```swift
while (<CONDITION>) {
    <LOOP CODE>
}

do {
    <LOOP CODE>
} while (<CONDITION>)
```
{% endtab %}

{% tab title="Swift" %}
```swift
while <CONDITION> {
    <LOOP CODE>
}

repeat {
    <LOOP CODE>
} while <CONDITION>
```
{% endtab %}
{% endtabs %}

### For Loop

{% tabs %}
{% tab title="Koltin" %}
```swift
for (<CONSTANT> in <RANGE>) {
    <LOOP CODE>
}
```
{% endtab %}

{% tab title="Swift" %}
```swift
for <CONSTANT> in <RANGE> {
    <LOOP CODE>
}
```
{% endtab %}
{% endtabs %}

#### Range

{% tabs %}
{% tab title="Koltin" %}
```kotlin
val closed = 0..5
// 0, 1, 2, 3, 4, 5

val halfOpenRange = 0 until 5
// 0, 1, 2, 3, 4

val descreaingRange = 5 downTo 0
// 5, 4, 3, 2, 1, 0 

val jumpRange = 0..5 step 2
// 0, 2, 4
```
{% endtab %}

{% tab title="Swift" %}
```swift
let closedRange = 0...5
// (0, 1, 2, 3, 4, 5)

let halfClosedRange = 0..<5
// (0, 1, 2, 3, 4)
```
{% endtab %}
{% endtabs %}

## When/Switch

Kotlin has no **Switch**, but has  **When**.

{% tabs %}
{% tab title="Koltin" %}
```kotlin
val hourOfDay = 12
val timeOfDay: String

timeOfDay = when (hourOfDay) {
    0 -> "Mid-night"
    1, 2, 3, 4, 5, 6 -> "Morning"
    in 7..18 -> "DayTime"
    hourOfDay == 19 -> "19 o'clock"
    else -> "Night"
}
```

Sometimes, we even don't add anything after when

```kotlin
when {
    number % 2 == 0 -> println("Even")
    else -> println("Odd")
}
```
{% endtab %}

{% tab title="Swift" %}
```swift
let hourOfDay = 12
let timeOfDay: String

switch hourOfDay {
case 0: 
    timeOfDay = "Mid-night"
case 1, 2, 3, 4, 5, 6:
    timeOfDay = "Morning"
case 7..<18:
    timeOfDay = "DayTime"
case _ where number == 19:
    timeOfDay = "19 o'clock"
case let x where x == 20:
    timeOfDay = "\(x) o'clock"
default:
    timeOfDay = "Night"
}
```
{% endtab %}
{% endtabs %}

