Gunel Balayeva

Arrays : 
Task 1.  Create an array of your favorite 5 movies

var myFavoriteMovies: [String] = ["The Intern", "Letters to Julie", "Bride Wars","The Bucket List","27 Dresses","The Proposal" ]
 
for myMovie in myFavoriteMovies {
    print(myMovie)
}

2. Print the first and last movie

var myFavoriteMovies: [String] = ["The Intern", "Letters to Julie", "Bride Wars", "The Bucket List", "27 Dresses", "The Proposal"]

if let firstMovie = myFavoriteMovies.first, let lastMovie = myFavoriteMovies.last {
    print("First movie:",firstMovie)
    print("Last movie:",lastMovie)
}

3. Add a new movie to do the  list
var myFavoriteMovies: [String] = ["The Intern", "Letters to Julie", 
"Bride Wars", "The Bucket List", "27 Dresses"]

//1. .append metodu ile:
 myFavoriteMovies.append("A Bronx Tale")

 // 2. append(contentsOf: ) metodu ile
 myFavoriteMovies.append(contentsOf: ["Midnight in Paris","The Devil Wears Prada"])

  print("My favorite movies list:",myFavoriteMovies)

4. Remove the second movie: 
var myFavoriteMovies: [String] = ["The Intern", "Letters to Julie", 
"Bride Wars", "The Bucket List", "27 Dresses"]

  print("My favorite movies list:",myFavoriteMovies)
 
  myFavoriteMovies.remove(at: 1)
  print("Removed list:",myFavoriteMovies)

5. Create an array of 6 different numbers
 var nums:[Int] = [10,20,30,40,50,60]
 print("Array of 6 different numbers:",nums)

6.Sort the array in ascending order

 // 1.  ic-ice for ile müqayisə:
var numbers: [Int] = [12, 45, 67, 89, 23, 56]

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

// 2. .sorted() metodu ile
var nums:[Int] = [20 ,30, 10, 40, 60, 50]
var sortedNums = nums.sorted()
print("Sorted array in ascending order:", sortedNums)

6. Find and print the second largest number

var numbers: [Int] = [10,20,30,40,50,60]

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



Sets :
1. Create a set 3 unique color
 var colors : Set<String> = ["Beige","Khaki","Olive"]
 print("Colors: ", colors)


2. Check if a specific color exists in the set

var colors: Set<String> = ["Beige", "Khaki", "Olive"]

if colors.contains("Khaki") {
    print("Yes, it is!")
} else {
    print("No, it is not!")
}

print("Colors:", colors)



Dictionary : 
Create a dictionary with 3 key-value pairs, where the key is a fruit name and the value is its price
          var fruits: [String: Double] = [ "Apple": 2.5,  "Banana": 3.5, "Orange": 3.0]

Print the price of one fruit
var fruits: [String: Double] = [ "Apple": 2.5,  "Banana": 3.5, "Orange": 3.0]

 if let price = fruits["Apple"] {
   print("1-ci mehsulun qiymet:",price) 
 } else {
     print("Bele bir mehsulu yoxdur!")
 }

Add a new fruit to the dictionary
var fruits: [String: Double] = [ "Apple": 2.5,  "Banana": 3.5, "Orange": 3.0]
 fruits["Kiwi"]=3.70
 print("Fruits:",fruits)
 






Conditionals(if, else, switch):

Create your age variable and print below conditions
Check “You are a child” if age<12
“You are a teenager” if age between 13-18
“You are an adult” otherwise 
let age = 12
// 1.  if-else şərti ilə
if age <= 12 {
    print("You are a child")
} else if age >= 13 && age <= 18 {
    print("You are a teenager")
} else {
    print("You are an adult")
}
Rewrite the function using a switch statement.
let age = 13
switch age {
    case  0...12: print("You are a child")
    case  13...18: print ("You are a teenager")
    default: print("You are an adult")
}

Create temperature variable and print below conditions
Prints “Cold” if temperature is below 10°C
Prints “Warm” if temperature is between 10°C and 25°C
Prints ”Hot” if temperature is above 25°C
  let temperature = 9
if temperature < 10 {
    print("Cold")
} else if temperature >= 10 && temperature <= 25 {
    print("Warm")
} else {
    print("Hot")
}

      4.Use a switch statement instead of if-else.
   let temperature = 30
 switch temperature {
     case ..<10:
      print("Cold")
     case 10...25:
     print("Warm")
     default : print("Hot")
 }
Optionals:
Create an optional String? variable and assign a name.
           let myName :String? = “Gunel”
 let myName :String?
 let myName :String? = nil
 Print its value using optional binding (if let).
let myName :String? 
myName = "Gunel"
if let checkName = myName {
    print("Ad teyin edilib:",checkName)
} else{
    print("Hec bir melumat tapilmadi")
}

 Print its value using optional binding (guard let).
// 1.  Birbasa koda tetbiqi - guard let
let myName: String? = "Gunel"
guard let checkName = myName else {
    print("Nill")
    exit(0)  
}
print("Ad teyin edilib:", checkName)
____________________________________
// 2. Parametrsiz metod ile guard let tetbiqi
func checkName() {
    let myName: String? = "Gunel"
    
        guard let checkName = myName else {
        print("Nill")
        return
    }
    
        print("Ad teyin edilib:", checkName)
}
checkName() 

 Assign nil to the variable and use the nil-coalescing operator (??) to
    provide a default value.
 let mynName:String? = nil
 let name = mynName ?? "Hec bir adlandirma  teyin edilmeyib"
 print(name)




Loops:
 Write a loop that prints numbers from 1 to 10.

for i in 1...10 {
    print(i)
}
 Write a loop that prints numbers from 10 to 1 using while.
//1. variable ile 10-1-e 
 var num = 10
while num >= 1 {
    print(num)
    number -= 1
} 
________________________ 
// array ile 10-1-e
var nums :[Int] = [1,2,3,4,5,6,7,8,9,10]
var i = nums.count - 1

while i >= 0{
    print(nums[i])
    i -= 1
}
 
Write a loop that prints every even number from 1 to 20.
 // 1. for ile (where istifade ederek)
for i in 1...20 where i % 2 == 0 {
    print(i)
}
_________________________________
// 2. for icinde if serti ile yoxlayaraq
for i in 1...20 {
   if (i % 2==0){
       print(i)
   }
}
         __________________________________
// 3. while icinde if serti ile yoxlayaraq
var i = 1
while i <= 20 {
    if i % 2 == 0 {
        print(i)
    }
    i += 1
}
___________________________________
// 3.repeat- while ile
var i = 2
repeat{
    print(i)
    i+=2
} while i <= 20

Write a repeat-while loop that generates a random number until it finds (Hint: Use Int.random(in: 1...10))

      var randomNumber: Int
      var count = 0            
repeat {
    randomNumber = Int.random(in: 1...10)
    count += 1
    print(count,". random eded:",randomNumber)
} while count < 10

Array Functions:
   1) Create an array of numbers: [2, 4, 6, 8, 10].
       var arr :[Int] = [2, 4, 6, 8, 10]
      print(arr)
   2) Find the maximum and minimum values. (Forbidden to use min(), max()
function)
// 1.  (Forbidden to use min(), max()function)
 var nums: [Int] = [2, 4, 6, 8, 10]
var min: Int = Int.max
var max: Int = Int.min

for i in nums {
    if i < min {
        min = i
    }
    if i > max {
        max = i
    }
}
print("Min value:", min)
print("Max value:", max)
___________________________
// 2. using min(),  max()
var nums: [Int] = [2, 4, 6, 8, 10]

if let min = nums.min(), let max = nums.max(){
   print("Min value:", min)
   print("Max value:", max) 
}

  3) Use .map() to create a new array where each number is doubled.
      let nums = [1, 2, 3, 4, 5]
     let doubledNums = nums.map { $0 * 2 }
     print(doubledNums)

  4) Use .filter() to keep only even numbers.
      let nums = [1, 2, 3, 4, 5]
     let filterNums = nums.filter { $0 % 2 == 0 }
     print(filterNums)

  5) Use .reduce() to find the sum of all numbers.
      let nums = [1, 2, 3, 4, 5]
     let reduceNums = nums.reduce(0) { $0 + $1 }
     print(reduceNums)

Extras:
Create a variable and check if the given word is a palindrome (same
forward and backward). If palindrome print “Word is palindrome”
otherwise print (“Not found”). Example:” racecar” → ✅ Word is
palindrome “hello” → ❌ Not found.
       
// 1. reversed() metodu ile

var word: String = "moM"
// Ya .lowercased() ile:
let staticWord:String = word.lowercased() 

//ve yaxud -> : .uppercased()metodu ile :
//let staticWord: String = word.uppercased() 

if staticWord == String(staticWord.reversed()) {
    print(staticWord, ": palindromdur")
} else {
    print(staticWord, ": deyildir") 
}
_________________________________

// 1. reversed metodu olmadan insert( at:) istifade ederek
var word: String = "moM"
let staticWord: String = word.lowercased()

var reversedWord = ""
for i in staticWord {
    reversedWord.insert(i, at: reversedWord.startIndex)
}
if staticWord == reversedWord {
    print(staticWord, ": palindromdur")
} else {
    print(staticWord, ": deyildir")
}
    
 Create a variable and check number is prime or not.
Print primeNumber if n is a prime number (only divisible by 1 and itself).
Otherwise print not prime Number .
     var number: Int = 7   
    var isPrime = true

if number <= 1 {
    isPrime = false 
} else {
    for i in 2..<number {
        if number % i == 0 {
            isPrime = false
            break
        }
    }
}

if isPrime {
    print("Sade ededdir:", number)
} else {
    print("Deyil")
}

Anagram Checker: Create two variables and check if two words are
anagrams (same letters, different order).
Example: “listen” and “silent”-> should print (“true”)
“hello” and “world” -> should pring(“false”)
  var word1: String = "listen"
var word2: String = "silent"

let sortedWord1 = String(word1.lowercased().sorted())
let sortedWord2 = String(word2.lowercased().sorted())

if sortedWord1 == sortedWord2 {
    print("true")
} else {
    print("false")
}
 Finds and returns the longest word in a sentence.
Example: given sentence is “Swift is an amazing programming
language”
Should print(“programming”)
 
let sentence = “Swift is an amazing programming language”

let splitWord = sentence.split(separator: " ")
var longestWord = ""

for word in splitWord {
    if word.count > longestWord.count {
        longestWord = String(word)
    }
}

print(longestWord)


