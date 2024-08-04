---
title: How to convert 'Char' to 'Int'
layout: single
categories: coding-test
tags: kotlin coding-test
toc: true
toc_icon: map-signs
toc_label: Table of Contents
---

Let's check out how to convert Char to Int, also oposite way!

Other data type in Kotlin, to convert data type,
we can use `to~~()` functions.

but if we want to convert `Char` 2 `Int`,
we should NOT use `toInt()` function.

Because if we use it, that method is going to return `ASCII code number`.

![](/images/toInt.png)

Also deprecated.
~~if you want to get ASCII code num, you can use it~~

Then,
what should we use for convert `Char type` 2 `Int`?

There's 3 ways to sole it!
Let's follow it!

# 1. convert to `String` first

let's see example code.

```kotlin
fun main() {  
    val char = '9'  
    //val char2Int = char.toInt() -> deprecated  

    val char2String2Int = char.toString().toInt()  
}
```

now you can do it!

but not totally recommended..
because there's 2 conversions.

# 2. use function (recommended)

```kotlin
fun main() {  
    val char = '9'  
    //val char2Int = char.toInt() -> deprecated  

    val char2Int = char.digitToInt()  
}
```

use `digitToInt()` function.

also, 
if char is not decimal digit, `Throws exception`
![](/images/digitToInt_docu.png)

[Link: digitToInt Official Document](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.text/digit-to-int.html)

# 3. use '0'

what a weird, right?

how to use '0'?

The answer is in at ASCII table.

Let's see
![](images/ascii_table.png)

Char '0' is Decimal 48.

Then,
if we want to get char's decimal, subtract '0' to char!

> `'0' - '0' = 0`
>
> `'1' - '0' = 1`
>
> `'2' - '0' = 2`
>
> ......

let's check sample code
```kotlin
fun main() {  
    val char = '9'  
    //val char2Int = char.toInt() -> deprecated  
    println(char.code) // -> 57
    println('0'.code) // -> 48
    val subtractionChar = char - '0'  // 9
}
```

