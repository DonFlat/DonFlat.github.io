---
title: Title of the post
description:
date: 2024/05/26
draft: true
tags: [Kotlin]
---
#### Swapping two numbers:
`a = b.also { b = a }` 
#### Char Array String
```
val s = "hello"
toCharArray()
```
#### Initialize an IntArray with filled values
`IntArray(amount + 1) { amount + 1 }`
#### Initialize an 3D array with fixed size
`val dp = Array(n) { Array(maxK + 1) { IntArray(2) } }`
#### Generate an array from a range
`(1..k).toList().toIntArray()`
#### Sort int array
`theIntArray.sort()`
`sorted = theIntArray.sortedArray()`
#### Deep copy a list
```
var newList = mutableListOf<Int>()
for (t in oledList) {
	newList.add(t)
}
totalList.add(newList)
```
#### ArrayDeque
```
add()
addFirst()
addLast()
clear()
contais()
removeFirst()
removeLast()
isEmpty()
```
#### Use LinkedList from Java for quicker insertion removal
**Actually, amortized is O(1), with Dynamic Array implementation**
#### Initialize a fixed 2D int array
```
val x = arrayOf(intArrayOf(1, 2), intArrayOf(3, 4))
```
#### What is a mutable list exactly?
`mutableListOf` produces an `ArrayList` 
#### downTo is two side inclusive
#### Map
```Kotlin[]
val m = mutableMapOf<Int, Int>('a' to 'b')
m.containsKey(k)
m.containsValue(v)
m[k] = m.getOrPut(k) {0} + 1 // This is equivalent to m[k]++ in C++ 

// for Map<Int, List>, doing this will work
val lis = m.getOrPut(k) { LinkedList<Int>() }
lis.add(i)
```
#### PQ
```Kotlin[]
val pq = PriorityQueue<Int> { a, b -> b - a }
val ts = TreeSet<IntArray> { a, b -> a[0] - b[0] }
```
#### Convert Char & String to Int
```
c.toInt()
```
#### Max value
`kotlin.Int.MAX_VALUE`
#### Convert array to String
```Kotlin[]
array.contentToString()
// notice: the string looks like a list
```
#### Extract all digits from an integer
```Kotlin[]
fun getDigits(number: Int): List<Int> { 
	var num = number 
	val digits = mutableListOf<Int>() 
	while (num != 0) { 
		val digit = num % 10 
		digits.add(digit) 
		num /= 10 
	} 
	return digits.reversed() 
}
```
#### Iterate with (index, value)
`for ((i, v) in nums.withIndex())`
#### Convert list to array
`lis.toTypedArray()`
#### Is a string +-*
```Kotlin[]
fun isOperator(str: String): Boolean {
	return "+-*/".contains(str)
}
```
#### LinkedList
```Kotlin[]
add()
addFirst() addLast()
first() last()
removeFirst() Last()
```
#### Use CharArray to mutate String
