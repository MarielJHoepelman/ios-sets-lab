# Sets lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

Ms. Gabriel Williams is a botany professor at District College. One day, she asked her student Mickey to compute the average of all the plants with distinct heights in her greenhouse.

Input: heights of trees below:
`161 182 161 154 176 170 167 171 170 174`

Output:
`169.375`

```swift
var inputArray = [161, 182, 161, 154, 176, 170, 167, 171, 170, 174]
var inputSet = Set(inputArray)
var sum = 0

for n in inputSet {
    sum = (n+sum)
}
var average = (Double(sum)/Double(inputSet.count))

print(average)
```


## Question 2

Determine if a String is a pangram. A pangram is a string that contains every letter of the alphabet at least once.

 e.g `"The quick brown fox jumps over the lazy dog"` is a pangram
 e.g `"The quick brown fox jumped over the lazy dog"` is NOT a pangram
 ```swift
 var InputString = "The quick brown fox jumped over the lazy dog"
 var abcString = "abcdefghijklmnopqrstuvwxyz"
 let abcSet = Set(abcString)
 let stringSet = Set(InputString)
 
 print(abcSet.isSubset(of: stringSet))
 ```


## Question 3

The set S originally contains numbers from 1 to n in ascending order. Unfortunately, due to the data error, one of the numbers in the set was duplicated to another number in the set. This results in the repetition of one number and loss of another number in the set.

You are given an array `nums` representing the data status of the set S after the error occurred. Your task is to first find the number occurs twice and then find the number that is missing from the sequence. Return these two values in the form of an array.

 Example 1:
 Input: `nums = [1,2,2,4]`
 Output: `[2,3]`

 Example 2:
 Input: `nums = [1,1]`
 Output: `[1,2]`

 Example 3:
 Input: `nums = [2,2]`
 Output: `[2,1]`


## Question 4

Given the 4 arrays of Ints below, create a new array, sorted in ascending order, that contains all the values without duplicates.

```swift
let arr1 = [2, 4, 5, 6, 8, 10, 12]
let arr2 = [1, 2, 3, 4, 5, 6]
let arr3 = [5, 6, 7, 8, 9, 10, 11, 12]
let arr4 = [1, 3, 4, 5, 6, 7, 9]

let arr1AsSet = Set(arr1)
let arr2AsSet = Set(arr2)
let arr3AsSet = Set(arr3)
let arr4AsSet = Set(arr4)

let setUnion = arr1AsSet.union(arr2AsSet).union(arr3AsSet).union(arr4AsSet)
print(setUnion)
let arrayWithNoDupes = Array(setUnion).sorted()
print(arrayWithNoDupes)
```


## Question 5

Perform the following set operations on the lists below:

1. Find the intersection and print the result
2. Find the symmetric difference and print the result
3. Find the union and print the result
4. What is the outcome of subtracting `list2` from `list1`? Print the result

```swift
let list1: Set = [1, 3, 4, 6, 2, 7, 9]
let list2: Set = [3, 7, 13, 10, 4]

print(list1.intersection(list2).sorted()) //prints [3, 4, 7]
print(list1.symmetricDifference(list2).sorted()) //prints [1, 2, 6, 9, 10, 13]
print(list1.union(list2).sorted()) //prints [1, 2, 3, 4, 6, 7, 9, 10, 13]
print(list1.subtracting(list2).sorted()) //prints [1, 2, 6, 9]
```


## Question 6

What output will be produced by the code below? Select one answer.

```swift
var spaceships = Set()

spaceships.insert("Serenity")
spaceships.insert("Enterprise")
spaceships.insert("TARDIS")
spaceships.insert("Serenity")

print(spaceships.count)

//This code will not compile. Spaceships compiler can't infer data type therefore var is not declared and inserts cannot be completed/printed.
```

- 3
- 4
- Nothing will be output
- 0
- This code will not compile
- 1
- This code will compile but crash


## Question 7

What output will be produced by the code below?

```swift
var spaceships1 = Set()

spaceships1.insert("Serenity")
spaceships1.insert("Enterprise")
spaceships1.insert("TARDIS")

let spaceships2 = spaceships1

if spaceships1.isSubset(of: spaceships2) {
  print("This is a subset")
} else {
  print("This is not a subset")
}

//This code won't compile because data type for 'var spaceships1 = Set()' cannot be infered by program.
```

- This code will compile but crash
- "This is not a subset"
- This code will not compile
- "This is a subset"
- Nothing will be output
