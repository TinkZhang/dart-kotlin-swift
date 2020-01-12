# Optional

```kotlin
var authorName: String?
```

### Force unwrapping

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
print("Name is ${authorName!!}")
```
{% endtab %}

{% tab title="Swift" %}
```swift
print("Name is \(authorName!)")
```
{% endtab %}
{% endtabs %}

App will crash if it's null.

Kotlin uses two **!!**, and Swift uses only one **!**

### Kotlin's Smart Cast and let\(\) function

Kotlin can add condition checker around the optional value, if it's not null, you can use it directly.

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
if (authorName != null) {
    println("Name is ${authorName}")
}
```
{% endtab %}
{% endtabs %}

let\(\) function accept lambda

```kotlin
authorName?.let {
    println("Name is ${authorName})
}
```

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

### Swift's **if-let** and guard-let-else

**if-let** focuses on what we what to do if it's not optional

And **guard-let-else** focuses on what we what to do if it's optional, and after the check, we can use this value directly.

{% tabs %}
{% tab title="Swift" %}
#### if-let

```swift
if let unwrappedAuthorName = authorName {
    print("Name is \(unwrappedAuthroName)")
} else {
    print("No Author")
}
```

Usually, we give the unwrapped constant the same name as the optional

```swift
if let authorName = authorName {
    print("Name is \(authorName)")
}
```

You can even unwrapped multiple values at the same time

```swift
if let authorName = authorName, 
    authorAge = authorAge, 
    authroAge > 18 {
        print("\(authorName) is \(authorAge) years old")
}    
```

#### guard-let-else

```swift
guard let authorName = authorName else {
    print("NO Name!!")
}
print("Name is ${authorName}")
```
{% endtab %}
{% endtabs %}

### Elvis operator

Kotlin use **?:** , while Swift use **??**

{% tabs %}
{% tab title="Kotlin" %}
```kotlin
var someAge: Int? = 10
var realAge = someAge ?: 0
```
{% endtab %}

{% tab title="Swift" %}
```swift
var someAge: Int? = 10
var realAge = someAge ?? 0
```
{% endtab %}
{% endtabs %}

