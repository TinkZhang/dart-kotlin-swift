# Collection

Collections are flexible containers that let your store any number of values together.

## Array & List

An array is an ordered collection of values of the same type.

#### Create an array

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
val evenNumbers = arrayOf(2, 4, 6, 8)
val fiveFives = Array(5, {5})
val zeors = DoubleArray(4)

```
{% endtab %}

{% tab title="Swift" %}
```swift
let evenNumber = [2, 4, 6, 8]
let subsriber: [String] = []
let allZeros = Array(repeating: 0, count: 5)
```
{% endtab %}
{% endtabs %}

#### List \(Kotlin\)

Array in Kotlin is fixed-size, so it can not grow or shrink. List is the option for that scenario.

#### Create an list

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
val innerPlanets = listOf("Mercury", "Venus", "Earth", "Mars")
// List is immutable

val outPlanets = mutableListOf("Jupiter", "Saturn", "Uranus", "Neptune")
val exoPlanets = mutableListOf<String>()
```
{% endtab %}
{% endtabs %}

## Map/Dictionary

A **map** \(Kotlin\) or **dictionary** \(Swift\) is an unordered collection of pairs, where each pair is comprised of a **key** and a **value**.

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
var yearOfBirth = mapOf("Anna" to 1990, "Bob" to 1992)
var namesAndScores = mutableMapOf("Anna" to 2, "Bob" to 4)
namesAndScores = mutableOf()

nameAndScores["Anna"]

// Property
nameAndScore.size
nameAndScore.isEmpty()
nameAndScore.get("Anna")

// Modify
namesAndScores["Coco"] = 4
namesAndScores.put("David", 2)
namesAndScores.remove("Anna")
namesAndScores.remove("Bob", 3)

// Iterate
for ((name, score) in namesAndScores) {
    println("$name - $score")
}
for (name in namesAndScores.keys) {
    println("$name, ")
}
```
{% endtab %}

{% tab title="Swift" %}
```swift
var nameAndScores = ["Anna": 2, "Bob": 4]
var pair: [String: Int] = [:]

nameAndScores["Anna"]

// Property
nameAndScores.isEmpty
nameAndScores.count

// Modify
nameAndScores["Coco"] = 4
nameAndScores.updateValue(4, forKey: "Anna")
nameAndScores.removeValue(forKey: "Bob")
nameAndScores["Coco"] = nil

// Iterate
for (name, score) in nameAndScores {
    print("\(name) - \(score)")
}
for name in nameAndScores.keys {
    print("\(name)")
}
```
{% endtab %}
{% endtabs %}

## Set

A set is an **unordered** collection of **unique** values of the same type.

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
val names = setOf("Anna", "Bob", "Coco")
val hashSet = HashSet<Int>()
val someArray = arrayOf(1, 2, 3, 1)
val someSet = setOf(*someArray)

println(someSet.contains(4))
println(3 in someSet)

someSet.add(4)
val removedOne: Boolean = someSet.remove(1)
```
{% endtab %}

{% tab title="Swift" %}
```swift
let setOne: Set<Int>
let someSet: Set<Int> = [1, 2, 3, 2] // it will be [1, 2, 3]

print(someSet.contains(4))

someSet.insert(5)
let removedElement: Int? = someSet.remove(1)
```
{% endtab %}
{% endtabs %}

