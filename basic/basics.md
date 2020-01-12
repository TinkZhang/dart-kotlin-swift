# Basics

## Variables/Constants

Modern languages treats variables and constants differently. For variable, its values can be modified. For constant, the value cannot change after assigned.

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
var age = 30
val name = "Tink"
```
{% endtab %}

{% tab title="Swift" %}
```swift
var age = 30
let name = "Tink"
```
{% endtab %}
{% endtabs %}

## Type

#### Type Inference

Kotlin and Swift work the same way for type inference.

## Pair/Triples and Tuple

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
val coordinates: Pair<Int, Double> = Pair(3, 1.33)
val coordinates = Pair(3, 1.33)
val coordinates = 3 to 1.33

val x = coordinates.first
val y = coordinates.second
val (x, y) = coordinates

val coordinates3D = Triple(2, 3, 1)
val (x, y, _) = coordinates3D
```
{% endtab %}

{% tab title="Swift" %}
```swift
let coordinates = (2, 3)
let x = coordinates.0
let y = coordinates.1

let (x, y) = coordinates
```
{% endtab %}
{% endtabs %}

Kotlin has type Pair and Triple.

It's **tuple** in Swift, it can be any length, as long as in \(\) and separated by ,

##  Special Type

{% tabs %}
{% tab title="Kotlin" %}
Any: mother of all other types \(except nullable types\)

Unit: a special type which only ever represents one value: the Unit object. It is similar to the void type in Java, except it makes working with generics easier

Nothing: a type that is helpful for declaring that a function not only doesn't return anything, but also never completes
{% endtab %}

{% tab title="Swift" %}

{% endtab %}
{% endtabs %}

## String Templates

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
val text = "world"
println("Hello, ${world}")
```
{% endtab %}

{% tab title="Swift" %}
```swift
let text = "world"
print("hello, \(world)")
```
{% endtab %}
{% endtabs %}

