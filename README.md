# Functions lab 1

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

Complete the function so that it will print out total cost after tax. Make sure to **call the function** afterwards.

```swift
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {

}
```

Then, modify the function you implemented to have a return type of `Int`, and use an external name that looks more readable. Function calls should look something like "total cost of the item after tax"

```swift
//Q1

//1.1
let itemCost = 45.0
let nyTax = 0.08775

func totalWithTax() {
    print(itemCost+(itemCost*nyTax))
}
totalWithTax()

//1.2
func totalCostOfTheItemAfterTax() -> Int{
    return Int(itemCost+(itemCost*nyTax))
}
print(totalCostOfTheItemAfterTax())
```


## Question 2

Convert the the following if/else statement below into function with a `String` return type.

```swift
let todaysTemperature = 72

if todaysTemperature <= 40 {
    print("It's cold out.")
} else if todaysTemperature >= 85 {
    print("It's really warm.")
} else {
    print("Weather is moderate.")
}
```
```swift
//Q2
let todaysTemperature = 72

func weather() -> String{

    if todaysTemperature <= 40 {
        return("It's cold out.")
    } else if todaysTemperature >= 85 {
        return("It's really warm.")
    } else {
        return("Weather is moderate.")
    }
}

print(weather())
```

## Question 3

Write a function named `min2` that takes two `Int` values, `a` and `b`, and returns the smallest one.

Function Definition
`func min2(a: Int, b: Int) -> Int`

Example:
Input: `min2(a:1, b:2)`

Output: `1`

```swift
func min2(a: Int, b: Int) -> Int{
    if a > b{
        return a
    }else{
        return b
    }
}
print(min2(a:1, b:2))
```

## Question 4

Write a function that takes an `Int` and returns its last digit. Name the function `lastDigit`. Use _ to ignore the external parameter name.

Function Definition:
`func lastDigit(_ number: Int) -> Int`

Example:
Input: `lastDigit(12345)`

Output: `5`

```swift
//Q4
func lastDigit(_ number: Int) -> Int{
    return number % 10
}

print(lastDigit(12345))
```

## Question 5

Write a function that takes in any two positive integers and return the sum.

```swift
//Q5
func sum(x: Int, y: Int) -> Int{
    return x+y
}
print(sum(x: 1, y: 2))
```
## Question 6

Write a function takes in any number grade and returns a corresponding letter grade.

| Number Grade | Equivalent Letter Grade |
| :--------: | :---------: |
| 100 | A+ |
| 90 - 99 | A |
| 80 - 89 | B |
| 70 - 79 | C |
| 65 - 69 | D |
| Below 65 | F |

```swift
//Q6
func letterGrade(x:Int) -> String{
    switch x {
        case 100:
            return "A+"
        case 90...99:
            return "A"
        case 80...89:
            return "B"
        case 70...79:
            return "C"
        case 65...69:
            return "D"
        default:
            return "F"
    }
}
print(letterGrade(x: 90))
```

## Question 7

Make a calculator function that takes in three parameters (two numbers and one operator) and returns the answer of the operation.

Operator parameter: (+, -, x, /)

```swift

func calculator(x:Double,y:Double,op:String) -> Double{
    switch op {
        case "+":
            return x + y
        case "-":
            return x - y
        case "*":
            return x * y
        case "/":
            return x / y
        default:
            return 0
    }
}
calculator(x: 2.0, y: 3.0, op: "*")
```


## Question 8

Write a function so that it will print out **total cost after tip.**

```swift
let mealCost = 45
let tipPercentage = 0.15

//Write your code below

let myFinalCost = totalWithTip() //Fill in the arguments
```

Write a function that will print out **total cost after tip and tax.**

```swift
let taxPercentage = 0.09

//Write your code below

let myFinalCostWithTipAndTax = totalWithTipAndTax() //Fill in the arguments in function
```
```swift

let mealCost = 45
let tipPercentage = 0.15
//8.1
func totalWithTip(mealC: Double, tip: Double) -> Double{
    return mealC+(mealC*tip)
}

let myFinalCost = totalWithTip(mealC: Double(mealCost), tip: tipPercentage)
//8.2
let taxPercentage = 0.09

func totalWithTipAndTax(withTip:Double) -> Double{
return withTip + (withTip*taxPercentage)
}

let myFinalCostWithTipAndTax = totalWithTipAndTax(withTip: myFinalCost)
print(myFinalCostWithTipAndTax)

```

## Question 9

Implement a function named `repeatPrint` that takes a string `message` and a integer `count` as parameters. The function should print `message` `count` number of times and then print a newline.

Example:
Input: `repeatPrint(message: "+", count: 10)`

Output: `++++++++++`


```swift 
//Q9
func repeatPrint(message:String, count:Int){
    let str = String(repeating: message, count: count  )
    print(str)
}
repeatPrint(message: "+", count: 10)

```


## Question 10

Write a function named `first` that takes an Int named n and returns an array with the first n numbers starting from 1.

Function Definition
`func first(_ n: Int) -> [Int]`

Example:
Input: `first(3)`

Output: `[1, 2, 3]`

```swift
func first(_ n: Int) -> [Int]{
    var result: [Int] = []
    for i in 1...n{
        result.append(i)
    }
    return result
}; print(first(3))

```
## Question 11

Write a function that prints the numbers from 1 to x, except:

If the number if a multiple of 3, print `"Fizz"` instead of the number
If the number is a multiple of 5, print `"Buzz"` instead of the number
If the number is a multiple of 3 AND 5, print `"FizzBuzz"` instead of the number
Your function should take in one parameter: x (the number to count up to)

```swift
func printUpToX(x: Int){
    for i in 1...x{
        if(i % 15 == 0){
            print("FizzBuzz")
        }else if i % 3 == 0{
            print("Fizz")
        }else if i % 5 == 0{
            print("Buzz")
        }else{
            print(i)
        }
    }
}
printUpToX(x: 30)
```

## Question 12

Write a function named `reverse` that takes an array of integers named `numbers` as a parameter. The function should return an array with the numbers from `numbers` in reverse order.


Example:
Input: `reverse([1, 2, 3])`

Output: `[3, 2, 1]`

```swift
func reverse(_ numbers:[Int]) -> [Int]{
    var result: [Int] = []
        for i in numbers{
        result.append(i)
    }
    return result
}

print(reverse([1, 2, 3]))
```

## Question 13

Write a function that prints out the most frequently appearing Int in an array of Int.

```swift
func mostFrequentInt(array: [Int]){
    var dictionary: [Int:Int] = [:]
    var counter = 0
    var mostFrequentInt = 0

    for i in array{
        if dictionary.keys.contains(i){
            dictionary.updateValue(dictionary[i]!+1, forKey: i)
        }else{
            dictionary[i] = 1
        }
    }

    for (key, value) in dictionary{
        if value > counter{
        counter = value
        mostFrequentInt = key
        }
    }
    print(mostFrequentInt)
}

mostFrequentInt(array: [1,1,1,1,1,2,2,2,3,4,4,5,5,5,5,5,5,5,5,5,5,5,5,5,5])

```

## Question 14

Write a function that sums all the even indices of an array of Ints.

```swift
func sumOfEvenIndices(array: [Int]) -> Int{
    var sum = 0
    for i in 0...array.count-1 where i % 2 == 0 {
        sum += array[i]
        print(array[i])
    }
    return sum
}
sumOfEvenIndices(array: [1,2,3,4,5])
```

## Question 15

Write a function that flips a dictionary.  All of the keys are now values and all of the values are now keys.

Example:
Input: `[1: "hi", 5: "bye:]`

Output: `["hi": 1, "bye": 5]`

```swift
func flipDict(_ dict: [Int:String]) -> [String:Int]{
    var newDict: [String:Int] = [:]
    for (key,value) in dict{
    newDict.updateValue(key, forKey: value)
}
return newDict
}
print(flipDict([1: "hi", 5: "bye"]))

```


## Question 16

Write a function that finds the person with the second highest test score in a Dictionary that maps names to scores.

Example:
Input: `["Person 1": 83, "Person 2": 74, "Person 3": 82]`

Output: `"Person 3"`

```swift
func findSecondHighestScore(dict: [String:Int]) -> String{
    var personWithHighestScore = String()
    var personWithSecondHighestScore = String()
    var highestScore = 0
    var secondHighestScore = 0

    for (key, value) in dict{
        if value > highestScore{
            if secondHighestScore < highestScore{
                secondHighestScore = highestScore
                personWithSecondHighestScore = personWithHighestScore
            }
        highestScore = value
        personWithHighestScore = key
        }
    }

        return personWithSecondHighestScore
}

print(findSecondHighestScore(dict: ["Person 1": 83, "Person 2": 74, "Person 3": 82]))
```

## Question 17

Write a function that determines if a value is inside of array.

```swift

func isValueInsideArray(_ value: Int, _ array: [Int]) -> Bool{

    for i in array{
        if value == array[i]{
        return true
        }
    }
    return false
}

print(isValueInsideArray(double: 3, double: [1,2,3,4,5,6]))
```

## Question 18

Write a function takes an `Int` as input, and returns true if it is even, or false if it is odd.
Using your new function, write code that prints out whether `dieRoll` is even or odd:

`let dieRoll = Int(arc4random_uniform(6) + 1)`

```swift

let dieRoll = Int(arc4random_uniform(6) + 1)

func isEven(_ x: Int) -> Bool{
    return x % 2 == 0
}

print(isEven(dieRoll))
```

## Question 19

Write a function that takes `[Int]` as input. It should return the largest Int in the array.

Using your function from the first step, use String interpolation to print a sentence that states what the largest Int in `myArray` is.

`let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]`

If you haven't already done so, write a function that takes in an Int and returns whether that number is even or odd. Use that function to print a sentence that states whether the largest Int in `myArray` is even or odd.

```swift
let myArray = [3,5,1,3,532,1,4,91,20,30,92,143]

func findLargestInt(_ array: [Int]) -> Int{
    var largestInt = 0

    for i in 0...array.count-1 where array[i] > largestInt{
        largestInt = array[i]
    }
    return largestInt
}

func isEven(_ x: Int) -> Bool{
    return x % 2 == 0
}

print(isEven(findLargestInt(myArray)))
```

## Question 20

Write a function that takes a String as input and returns the number of characters in the string

Using your function, print how many characters are in myString:

`let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."`

```swift
let myString = "Swift is a new programming language for iOS, OS X, watchOS, and tvOS apps that builds on the best of C and Objective-C, without the constraints of C compatibility."

func numOfCharacterst(_ str:String) -> Int{
    return str.count
}

print(numOfCharacterst(myString))
```

## Question 21

Write a function that counts how many characters in a String match a specific character.  (e.g: count how many "a"s are in a String, or count how many ","s are in a String.

Example:
Input:
```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"
```
Sample output: `3`

```swift
let testString = "This is a test string for your code"
let targetCharacter: Character = "i"

func characterCount(str:String, char:Character) -> Int{

var dictionary: [Character:Int] = [:]

for c in str{
    if dictionary.keys.contains(c){
        dictionary.updateValue(dictionary[c]!+1, forKey: c)
    }else{
        dictionary[c] = 1
    }
}

return dictionary[char]!
}

print(characterCount(str: testString, char: "i"))
```

## Question 22

Write a function that counts how many characters in a String match one of several possible characters.  (e.g: count how many vowels are in a String, or count how many "a"s "b"s and "c"s are in a Sting)

Example:
Input:
```swift

```
```swift
let inputString = "This one is a little more complicated"
let targetCharacters: [Character] = ["a","e","i","o","u"]

func numChar(_ str: String,_ target:[Character] ) -> Int{
var counter: Int = 0

for c in str{
if target.contains(c){
counter += 1
}
}

return counter
}
numChar(inputString, targetCharacters)
```

Output: `13`


## Question 23

Write a function that returns the number of unique Ints in an array of Ints.

Example:
Input: `let inputArray2 = [3,1,4,1,3,2,6,1,9]`

Output: `4`

//Explanation: 2, 4, 6, 9 are unique in the array. Every other number is not unique.

```swift
//Q23 
let inputArray2 = [3,1,4,1,3,2,6,1,9]

func numOfUniqueInt(_ input: [Int]) -> Int{
    var counter = 0
    var dict = [Int:Int]()

    for i in input{
        if dict.keys.contains(i){
        dict.updateValue(dict[i]!+1, forKey: i)
        }else{
            dict[i] = 1
        }
    }

    for (_, value) in dict{
        if value == 1{
        counter += 1
        }
    }
return counter
}

print(numOfUniqueInt(inputArray2))
```

## Question 24

Write a function that converts a binary number into decimal. The binary number will be given as an array of Ints.

Example:
Input: `let binaryArray = [1,0,1,1,1,0,1]`
Output: `93`

```swift
let binaryArray = [1,0,1,1,1,0,1]

func toDecimal(_ input: [Int]) -> Decimal{
    var output = Decimal()
    //  let flip = input.reversed()
    var index = 0

    for i in input.reversed(){
        output += Decimal(i)*pow(2,index)
        index += 1
    }

    return output
}

print(toDecimal(binaryArray))
```



## Question 25

Write a function named `timeDifference`. It takes as input four numbers that represent two times in a day and returns the difference in minutes between them. The first two parameters `firstHour` and `firstMinute` represent the hour and minute of the first time. The last two `secondHour` and `secondMinute` represent the hour and minute of the second time. All parameters should have external parameter names with the same name as the local ones.

Example:
Input: `timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10)`

Output: `67`

```swift

func timeDifference(firstHour: Int, firstMinute: Int, secondHour:Int, secondMinute:Int) -> Int {
    var answerInMinutes = 0
    var hourDifference = 0
    var minuteDifference = 0

    hourDifference = secondHour - firstHour

    if(secondMinute > firstMinute){
        minuteDifference = secondMinute - firstMinute
    }else{
    hourDifference -= 1
    minuteDifference = (secondMinute+60)-firstMinute
    }

    answerInMinutes = (hourDifference*60)+minuteDifference

    return answerInMinutes
}

print(timeDifference(firstHour: 12, firstMinute: 3, secondHour: 13, secondMinute: 10))

```

## Question 26

Write a function called `filterOdd` that takes an array of ints and returns it with just the even numbers.

Example:
Input:  `filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8])`

Output: `[2, 4, 6, 8]`

```swift
func filterOdd(arr:[Int]) -> [Int]{
    var answer = [Int]()
for i in arr where i % 2 == 0{
    answer.append(i)
}
    return answer
}
print(filterOdd(arr: [1, 2, 3, 4, 5, 6, 7, 8]))

```
## Question 27

Write a function called `doubleIt` that takes an array of ints and returns it with all the elements doubled.

Example:
Input: `doubleIt(arr: [1, 2, 3, 4])`

Output: `[2, 4, 6, 8]`

```swift
//Q27
func doubleIt(arr: [Int]) -> [Int]{
var answer = [Int]()

for i in arr{
    answer.append(i*2)
}

return answer
}

print(doubleIt(arr: [1, 2, 3, 4]))
```


Then write a function called `multiplyBy` that takes an array of ints and an int n that will return the array with all the elements multiplied by n.

Example:
Input:  `multiplyIt(arr: [1, 2, 3, 4], n: 4)`

Output:  `[4, 8, 12, 16]`

```swift
func multiplyIt(arr: [Int],n: Int) -> [Int]{
    var answer = [Int]()

for i in arr{
    answer.append(i*n)
}

return answer
}
print(multiplyIt(arr: [1, 2, 3, 4], n: 4))
```

## Question 28

Write a function called `unwrap` that takes an array of optional ints and returns an array with them unwrapped with any nil values removed.

Example:
Input:  `unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2])`

Output: `[7, 4, 43, 11, 2]`

```swift
func unwrap(arr: [Int?]) -> [Int]{
    var output = [Int]()
    for i in arr{
        if let x = i{
        output.append(x)
        }
    }
    return output
}
print(unwrap(arr: [nil, 7, 4, nil, 43, 11, nil, 2]))
```

## Question 29

Write a function that takes an array of bools and returns a dictionary that maps the bools to how many times they appear in the array.

Example:
Input:  `countBools(arr: [true, true, false, true, false, true])`

Output: `[false: 2, true: 4]`

```swift
func countBools(arr: [Bool]) -> [Bool:Int]{
    var boolDict = [Bool:Int]()

    for i in arr{
        if boolDict.keys.contains(i){
            boolDict.updateValue(boolDict[i]! + 1, forKey: i)
        }else{
            boolDict[i] = 1
        }
    }
    return boolDict
}

print(countBools(arr: [true, true, false, true, false, true]))
```

## Question 30

Write a function that takes a string as input and returns a dictionary that maps each unique character to how many times they appear in the string.

Example:
Input:  `countCharacters(str: "Hello, World!")`

Output: `["H": 1, "r": 1, "!": 1, "e": 1, "o": 2, "l": 3, ",": 1, " ": 1, "W": 1, "d": 1]`

```swift
func countCharacters(str: String) -> [Character:Int]{
    var output = [Character:Int]()

    for char in str{
        if output.keys.contains(char){
            output.updateValue(output[char]!+1, forKey: char)
        }else{
            output[char] = 1
        }
    }
    return output
}
print(countCharacters(str: "Hello World!"))
```
## Question 31

31
Write a function that takes this dictionary of baseball teams by ID and returns an array of tuples that contain each team's ID and name.

`let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]`

Example:
Input:  `dictToTuples(dict: baseballTeamsById)`

Output: `[(.0 1003, .1 "Rays"), (.0 1001, .1 "Mets"), (.0 1004, .1 "Marlins"), (.0 1002, .1 "Yankees")]`

```swift
let baseballTeamsById = [1001:"Mets", 1002:"Yankees", 1003:"Rays", 1004:"Marlins"]

func dictToTuples(dict: [Int:String]) -> [(Int, String)]{
var output = [(teamID:Int, teamName:String)]()

for (key, value) in dict{
output.append((key,value))
}
return output
}

print(dictToTuples(dict: baseballTeamsById))
```

## Question 32

Write a function that checks if a String is a [Palindrome](https://en.wikipedia.org/wiki/Palindrome)

```swift
func isPalindrome(str: String) -> Bool{
    let reverseStr = String(str.reversed())
    return str == reverseStr
}
print(isPalindrome(str: "abba"))
```
## Question 33

Write a function that checks if a String is a [pangram](https://en.wikipedia.org/wiki/Pangram)

```swift
var str = "The quick brown fox jumps over the lazy dog"

func isPangram(input:String) -> Bool{
    var alphabet = Set("abcdefghijklmnopqrstuvwxyz")

    for char in str.lowercased(){
        alphabet.remove(char)
    } //Removing the letter for the alphabet set when comming across it in the string

    //The alphabet set should be completely empty if the string is a panagram

    if alphabet.isEmpty{
        return true
    }else{
        return false
    }
}
print(isPangram(input: str))

```

## Question 34

Write your own `min()` and `max()` functions for an Array of Ints

```swift
func maximum(input: [Int]) -> Int{
    var output: Int = 0
    for i in input{
        if i > output{
        output = i
        }   
    }
    return output
    }

func minimum(input: [Int]) -> Int{
    var output: Int = input[0]
    for i in input{
        if i < output{
        output = i
        }
    }
return output
}

print(maximum(input: [1,2,3,4,5,6,7,8,9,8,7,6]))
print(minimum(input: [1,2,3,4,5,6,7,8,9,8,7,6]))


```


## Question 35

Given two arrays of Ints, write a function that tells you all the values they have in common.

```swift
func common(arr1:[Int], arr2:[Int]) -> Set<Int>{
    var answer = Set<Int>()
    answer = Set(arr1).intersection(Set(arr2))
    return answer
}

print(common(arr1: [1,2,3,4], arr2: [3,4,5,6]))
```

## Question 36

Find the most-frequently appearing Array of Ints in an Array of Arrays of Ints.

```swift
func mostFrequentArrayOfIntsInAnArrayOfInts(input: [[Int]]) -> [Int]{
    var output = [Int]()
    var dict = [[Int]:Int]()
    var highestValue = 0

    for i in input{
        if dict.keys.contains(i){
            dict.updateValue(dict[i]!+1, forKey: i)
        }else{
            dict[i] = 1
        }
    }
    for (key,value) in dict{
        if value > highestValue {
            highestValue = value
            output = key
        }
    }
return output
}
var test = [[1,2,3],[1,2,3],[2,2],[1,2,3,4],[2,2],[2,2],[2,3,4,5],[1,2,3],[2,2]]

print(mostFrequentArrayOfIntsInAnArrayOfInts(input: test))
```

## Question 37

Given a String as input, rotate all a-z characters by one.  This is called [ROT-1 encryption](http://www.rot-n.com/).

Sample input:
`This is a test string. Anything can be written in here (even Zebras and zebras).`

Sample output:
`Uijt jt b uftu tusjoh. Bozuijoh dbo cf xsjuufo jo ifsf (fwfo Afcsbt boe afcsbt).`

```swift

var str = "This is a test string. Anything can be written in here (even Zebras and zebras)."

func caesarCipher(message: String, shift: Int) -> String{
    var encryptedMessage = String()

    for c in message{

        let ans = String(UnicodeScalar(Int(c.asciiValue!)+shift)!)
        encryptedMessage.append(ans)

    }

return encryptedMessage
}
print(caesarCipher(message: "Hello World!", shift: 10))
```
