To organize your code for sharing on GitHub in a clean and structured manner, here's a formatted version of your content:

---

# Swift Practice: Arrays, Sets, Dictionaries, and More

This repository contains exercises to practice Swift fundamentals, such as arrays, sets, dictionaries, conditionals, loops, optionals, and more.

## Arrays

### 1. Create an Array of Your Favorite 5 Movies
```swift
var myFavoriteMovies: [String] = ["The Intern", "Letters to Julie", "Bride Wars", "The Bucket List", "27 Dresses", "The Proposal"]
for myMovie in myFavoriteMovies {
    print(myMovie)
}
```

### 2. Print the First and Last Movie
```swift
if let firstMovie = myFavoriteMovies.first, let lastMovie = myFavoriteMovies.last {
    print("First movie:", firstMovie)
    print("Last movie:", lastMovie)
}
```

### 3. Add a New Movie to the List
```swift
myFavoriteMovies.append("A Bronx Tale")
myFavoriteMovies.append(contentsOf: ["Midnight in Paris", "The Devil Wears Prada"])
print("My favorite movies list:", myFavoriteMovies)
```

### 4. Remove the Second Movie
```swift
myFavoriteMovies.remove(at: 1)
print("Removed list:", myFavoriteMovies)
```

### 5. Create an Array of 6 Different Numbers
```swift
var nums: [Int] = [10, 20, 30, 40, 50, 60]
print("Array of 6 different numbers:", nums)
```

### 6. Sort the Array in Ascending Order
- **Using a loop:**
```swift
var temp: Int
for i in 0..<numbers.count {
    for j in i+1..<numbers.count {
        if numbers[i] > numbers[j] {
            temp = numbers[i]
            numbers[i] = numbers[j]
            numbers[j] = temp
        }
    }
}
print("Sorted array in ascending order:", numbers)
```
- **Using `.sorted()` method:**
```swift
var sortedNums = nums.sorted()
print("Sorted array in ascending order:", sortedNums)
```

### 7. Find and Print the Second Largest Number
```swift
var largest = Int.min
var secondLargest = Int.min
for number in numbers {
    if number > largest {
        secondLargest = largest
        largest = number
    } else if number > secondLargest && number != largest {
        secondLargest = number
    }
}
print(secondLargest)
```

## Sets

### 1. Create a Set with 3 Unique Colors
```swift
var colors: Set<String> = ["Beige", "Khaki", "Olive"]
print("Colors:", colors)
```

### 2. Check if a Specific Color Exists in the Set
```swift
if colors.contains("Khaki") {
    print("Yes, it is!")
} else {
    print("No, it is not!")
}
```

## Dictionary

### 1. Create a Dictionary with 3 Key-Value Pairs
```swift
var fruits: [String: Double] = ["Apple": 2.5, "Banana": 3.5, "Orange": 3.0]
```

### 2. Print the Price of One Fruit
```swift
if let price = fruits["Apple"] {
    print("1-ci mehsulun qiymet:", price)
} else {
    print("Bele bir mehsulu yoxdur!")
}
```

### 3. Add a New Fruit to the Dictionary
```swift
fruits["Kiwi"] = 3.70
print("Fruits:", fruits)
```

## Conditionals (`if`, `else`, `switch`)

### 1. Create Your Age Variable and Print Conditions
```swift
let age = 12
if age <= 12 {
    print("You are a child")
} else if age >= 13 && age <= 18 {
    print("You are a teenager")
} else {
    print("You are an adult")
}
```

### 2. Rewrite the Function Using a Switch Statement
```swift
switch age {
    case 0...12: print("You are a child")
    case 13...18: print("You are a teenager")
    default: print("You are an adult")
}
```

### 3. Temperature Conditions
```swift
let temperature = 9
if temperature < 10 {
    print("Cold")
} else if temperature >= 10 && temperature <= 25 {
    print("Warm")
} else {
    print("Hot")
}
```

### 4. Use a Switch Statement for Temperature
```swift
switch temperature {
    case ..<10: print("Cold")
    case 10...25: print("Warm")
    default: print("Hot")
}
```

## Optionals

### 1. Optional Binding with `if let`
```swift
let myName: String? = "Gunel"
if let checkName = myName {
    print("Ad teyin edilib:", checkName)
} else {
    print("Hec bir melumat tapilmadi")
}
```

### 2. Optional Binding with `guard let`
```swift
guard let checkName = myName else {
    print("Nill")
    exit(0)
}
print("Ad teyin edilib:", checkName)
```

### 3. Use Nil-Coalescing Operator
```swift
let mynName: String? = nil
let name = mynName ?? "Hec bir adlandirma  teyin edilmeyib"
print(name)
```

## Loops

### 1. Loop that Prints Numbers from 1 to 10
```swift
for i in 1...10 {
    print(i)
}
```

### 2. Loop that Prints Numbers from 10 to 1 Using `while`
```swift
var num = 10
while num >= 1 {
    print(num)
    num -= 1
}
```

### 3. Print Every Even Number from 1 to 20
```swift
for i in 1...20 where i % 2 == 0 {
    print(i)
}
```

### 4. Repeat-While Loop that Generates a Random Number
```swift
var randomNumber: Int
var count = 0
repeat {
    randomNumber = Int.random(in: 1...10)
    count += 1
    print(count, ". random eded:", randomNumber)
} while count < 10
```

## Extras

### 1. Palindrome Check
```swift
var word: String = "moM"
let staticWord = word.lowercased()

if staticWord == String(staticWord.reversed()) {
    print(staticWord, ": palindromdur")
} else {
    print(staticWord, ": deyildir")
}
```

### 2. Prime Number Check
```swift
var number: Int = 7
var isPrime = true
for i in 2..<number {
    if number % i == 0 {
        isPrime = false
        break
    }
}

if isPrime {
    print("Sade ededdir:", number)
} else {
    print("Deyil")
}
```

---

This structure should make it easy to share and read your code on GitHub. Let me know if you need any adjustments!
