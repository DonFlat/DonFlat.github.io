---
title: Java CheatSheet
description: Common Java operations in LeetCode
date: 2024-05-26
draft: false
tags: [Java]
---
#### Queue
```
Queue<Integer> q = new LinkedList<Integer>();
q.add()
q.poll()
q.size()
```
#### Set
```
Set<Integer> s = new HashSet<Integer>();
s.add()
s.contains()
s.isEmpty()
s.remove()
s.size()
```
#### Strings
```
// Split string
String[] s = str.split(" ")
```
#### Read from keyboard input
```
Scanner scanner = new Scanner(System.in); 
System.out.println("Enter your name: "); 
String name = scanner.nextLine();
```
    
#### Use args
```
for (String arg : args) { 
	System.out.println(arg); 
}
```

#### Find peak in array
```
int maxVal = Arrays.stream(nums).max().getAsInt();
// complexity vs looping through: same, O(n). stream scan through underneath
// Just a higher level abstraction
```
#### Fill array
```
int[] nums = new int[n];
Arrays.fill(nums, x);
```
**! it is different from explicitly iterating over element and assign new objects**
### PQ
```
TreeSet<int[]> pq = new TreeSet<>((a, b) -> { return distance(a) - distance(b); });
```
### HashMap
```
m.put(k, m.getOrDefault(k, 0) + 1)
m.forEach((k, v) -> );
for (Map.Entry<K, V> entry : m.entrySet())
```
### Max int
`Integer.MAX_VALUE`
### String operations
```
char c = s.charAt(i)
for (char c : s.toCharArray())
```
#### Custom sort
```
Arrays.sort(intervals, (a, b) -> { return a[0] - b[0]; });
```
#### Frequent string <-> number
```
str = Integer.toString(number)
number = Integer.ParseInt(str)
```
#### Concate array of String
`String.join("", str_array)`
#### Convert list into array
`res.stream().mapToInt(Integer::intValue).toArray()`
#### Use stream to calc sum of length of strings in list
`stack.stream().mapToInt(String::length).sum()`
#### Queue: offer vs add, remove vs poll, etc
[Java Interface Queue](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html#offer-E-)
The methods provide similar functionalities, but differ in behavior. One throws exception if fail to do so, the other returns special value (`null`/`false`).
`add`throws exception.`offer`returns `false`.
**Why this difference?** The latter more frequent used in bounded context, like sized queue, where insertion failure is common.
#### Convert a numerical string into a number
```
s = "114514"
var res = 0;
for (int i = 0; i < s.len; i++) {
	res = res * 10 + s.charAt(i) - '0';
}
```
#### Convert a char array into String
```
var charArray = new char[26];
String(charArray);
```