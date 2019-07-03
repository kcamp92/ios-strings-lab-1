# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)

var emptyString = ""
let int = 1...10
for a in int {
emptyString += String(a)
}
print(emptyString)
***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

var emptyString = ""
let int = 5...51

for a in int {
if a % 2 == 0 {
emptyString += " \(a) "
}
}
print(emptyString)

***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

var emptyString = ""

let range = 1...60
let maxNumber = 60
var initialNumber = 4

for _ in range where initialNumber < maxNumber {
initialNumber += 10

emptyString += "\(initialNumber) "
}
print(emptyString)
***
## Question 4

Print each character in the string `"Hello world!"`

let string = "Hello world!"
for character in "Hello world!"{
print(character)
}
***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

var myStringSeven = "Hello world!"
myStringSeven = String((myStringSeven.last)!)

print(myStringSeven)


***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

let stringOne = "summerj"
var count = 0
var checkin = stringOne.count % 2 == 0

switch checkin {
case true:
for char in stringOne {
print(char)
}
case false:
for char in stringOne {
count += 1
if count % 2 != 0 {
print(char)
}
}
}
***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

var stringOne: Character = "a"
stringOne == Character("a")

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

var accentedLetter = "\u{65}\u{0301}"
print(accentedLetter)

var hungry =  "é"
print(hungry == accentedLetter)

var accentedLetters = "\u{61}\u{0301}"
print(accentedLetters)

var hunger =  "á"
print(hunger == accentedLetters)

var accentedLettering = "\u{6f}\u{0301}"
print(accentedLettering)

var hangry =  "ó"
print(hangry == accentedLettering)

var accentedLett = "\u{69}\u{0301}"
print(accentedLett)

var hang =  "í"
print(hang == accentedLett)

var accentedLow = "\u{75}\u{0301}"
print(accentedLow)

var hand =  "ú"
print(hand == accentedLow)


***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

let unicodeHello = "\u{48}\u{65}\u{6c}\u{6c}\u{6f}"
let unicodeWorld = "\u{57}\u{6f}\u{72}\u{6c}\u{64}\u{21}"
print(unicodeHello + " " + unicodeWorld)
***
I realized afterwards that I was supposed to print out all CAPS.

## Question 10

**Using only Unicode**, print out your name.

let unicodeKrystal = "\u{4b}\u{72}\u{79}\u{73}\u{74}\u{61}\u{6c}"
let unicodeCampbell = "\u{43}\u{61}\u{6d}\u{70}\u{62}\u{65}\u{6c}\u{6c}"
print(unicodeKrystal + " " + unicodeCampbell)

***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

let unicodeHola = "\u{48}\u{6f}\u{6c}\u{61}"
let unicodeMundo = "\u{4d}\u{75}\u{6e}\u{64}\u{6f}"
print(unicodeHola + " " + unicodeMundo)
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```
var flower = "\u{2698}"
var verticalSymbol = "\u{007c}"
var horizontalSymbol = "\u{005f}"

for _ in 1...11 {
print(horizontalSymbol, terminator: " ")
}
print()
print()

for _ in 1...7 {
print("\(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol) \(flower) \(verticalSymbol)")
}
***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```
var chessBoard = "\u{43}\u{68}\u{65}\u{73}\u{73}\u{20}\u{42}\u{6f}\u{61}\u{72}\u{64}:"
print(chessBoard)


let unicodePlayerRoyal = "\u{2656}\u{2658}\u{2657}\u{2655}\u{2654}\u{2657}\u{2658}\u{2656}"
print(unicodePlayerRoyal, separator: " ")
let unicodePlayerPawns = "\u{2659}"
for _ in 1...8 {
print(unicodePlayerPawns, terminator: " ")
}
print()
print()
print()

let unicodePlayerTwoPawns = "\u{265f}"
for _ in 1...8 {
print(unicodePlayerTwoPawns, terminator: " ")
}
print()

let unicodePlayerTwoRoyal = "\u{265c}\u{265e}\u{265d}\u{265b}\u{265a}\u{265d}\u{265e}\u{265c}"

print(unicodePlayerTwoRoyal)

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

var aString = "Replace the letter e with *"

var replacedString = " "
replacedString +=
aString.replacingOccurrences(of: "e", with: "*")
print(replacedString)

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

// Your code here
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

var aString = "this string has 29 characters"
var reversedString = " "
reversedString +=
aString.reversed()
print(reversedString)

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here
```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

let aString = "madam"
var reversedString = ""
for letters in aString {
reversedString = "\(letters)" + reversedString
}
if reversedString == aString {
print("true")
}   else {
print("false")
}

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```
var sentence = "split this string into words and print them on separate lines "
var space = " "
var currentWord = ""

for character in sentence {
if String (character) == space {
print(currentWord)
currentWord = ""
continue
}
currentWord += String(character)
}
***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

var problem = "find the longest word in the problem description"
var split = problem.components(separatedBy: " ")

var max = split.max(by: { $1.count > $0.count})
if max != nil {
print((max)!)
}

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"



func vowelConsonants(_ input: String) -> (vowels: Int, consonants: Int) {
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
var vowelCount = 0
var consonantCount = 0

for letter in input.lowercased() {
if consonants.contains(letter) {
consonantCount += 1
} else {
if vowels.contains(letter) {
vowelCount += 1
}
}
}
return (vowelCount, consonantCount)
}
print(vowels.count)
***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`
let phrase = "How are you doing this Monday?"
let wordCount = phrase.filter{ $0.isLetter || $0.isWhitespace }
if let index = wordCount.lastIndex(of: " ") {
let lastWord = wordCount[index...]
print(lastWord.count)
} else {
print("No last word")
}

***
