---
title: Convert int to various radix
layout: single
categories: coding-test
tags: kotlin coding-test
toc: true
toc_icon: map-signs
toc_label: Table of Contents
---
<font color="#c0504d">Is there somone who doesn't know radix,</font>


[Link: wikipedia-radix](https://en.wikipedia.org/wiki/Radix)

<font color="#c0504d">check this first.</font>

---

[Link: toString(radix), Kotlin Official Docu](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.text/to-string.html)

**only Int can convert to Radix String**

# Int to various radix byte

first, if you have `Int number`, 
use `toString(radix: Int)` to convert String but radix byte.

```kotlin
fun main() {  
    val int = 105  
    println("binary: ${int.toString(2)}") // binary  
    println("ternary byte: ${int.toString(3)}") // ternary byte  
    println("octal: ${int.toString(8)}") // octal  
    println("decimal: ${int.toString(10)}") // decimal, not necessary to use  
    println("hexadecimal: ${int.toString(16)}") // hexadecimal
}
```
![](../images/toString(radix).png)


# various radix byte to Int

now, time to convert other side

use `toInt(radix: Int)`! EASYEASY~

[Link: toInt(radix)), Kotlin Official Docu](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.text/to-int.html)

```kotlin
fun main() {  
    val binary = "1101001"  
    val ternary = "10220"  
    val octal = "151"  
    val decimal = "105"  
    val hexadecimal = "69"  
  
    println("binary($binary) -> Int: ${binary.toInt(2)}")  
    println("ternary byte($ternary) -> Int: ${binary.toInt(2)}")  
    println("octal($octal) -> Int: ${binary.toInt(2)}")  
    println("decimal($decimal) -> Int: ${binary.toInt(2)}")  
    println("hexadecimal($hexadecimal) -> Int: ${binary.toInt(2)}")  
}
```

![](../images/toInt(radix).png)