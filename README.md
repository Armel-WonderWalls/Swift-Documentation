# Swift Documentation
## 1. What is Swift?
Swift is the language developed by Apple to replace Objective-C which was criticized for being hard to learn and had weird syntax.  
It's advertised as "fast, modern, safe and interactive".
#### Objective-C
```objective-c
const int count = 10;
double price = 23.55;

NSString *firstMessage = @"Swift is awesome. ";
NSString *secondMessage = @"What do you think?";
NSString *message = [NSString stringWithFormat:@"%@%@", firstMessage, secondMessage];

NSLog(@"%@", message);
```
#### Swift
```swift
let count = 10
var price = 23.55

let firstMessage = "Swift is awesome. "
let secondMessage = "What do you think?"
var message = firstMessage + secondMessage

print(message)
```
## 2. Type Inference
Swift allows us to not specify type when declaring a variable/constant.  
The compiler can deduce the type by examining the default value of the variable/constant.
```swift
var expliciteTypeInteger : Int = 10
var inferencedTypeIntgeger = 10
```
## 3. String Interpolations
String interpolations is the recommended way to build a string from multiple types.  
You wraps the variable for string conversion in parentheses, prefixed by a backslash.
```swift
var totalPrice = 9.99
var typeConversionMessage = "The price of the book is $" + String(totalPrice)
var stringInterpolationMessage = "The price of the book is $ \(totalPrice)"
```
## 4. Control Flow
List of all the control flow statements
#### ***for-in*** loop
```swift
for item in collection {
    print("item")
}
```
#### ***while*** loop
```swift
while condition {
    print("print this while condition is true")
}
```
#### ***repeat-while*** loop
```swift
repeat {
    print("print this once, then print this again while condition is true")
} while condition
```

## 5. Conditional Control Flow
List of all the conditional control flow statements
#### ***if*** statement
```swift
if condition {
  print("condition is true")
}
```
#### ***if-else*** statement
```swift
if condition {
  print("condition is true")
} else {
  print("condition is false")
}
```
#### consecutive ***if-else*** statements
```swift
if conditionA {
  print("conditionA is true")
} else if {
  print("conditionB is true")
} else {
  print("conditionA and conditionB are false")
}
```
#### ***switch*** statement
```swift
switch value {
case 1:
  print("value equal 1")
case 2, 3:
  print("value equal 2 or 3")
case 4...6:
  print("value equal 4, 5 or 6")
case 7..<10:
  print("value equal 7, 8 or 9")
default:
  print("value is not in the range from 1 to 9.")
}
```
Notes: 
Cases can match many different patterns, including interval matches, tuples, and casts to a specific type.  
Matched values in a switch case can be bound to temporary constants or variables for use within the case’s body, and complex matching conditions can be expressed with a ***where*** clause for each case.
## Optionals
To use optionals variable you need to implicitly asign type to the variable and adding question mark (?) at the end of it.
```swift
var optionalVariable : String?
```
An optional variable can either have a value of it's type or being empty ("nil").
#### Forced unwrapping
We can use the exclamation mark (!) to force the compiler to use an optional variable.
```swift
print(optionalVariable!)
```
#### Optional Binding
Before using an optional variable you need to check if it have a value or if it's empty ("nil").  
The recommanded way is to use optional binding with the ***if-let*** statement.  
If `optionalVariable` have a value, the value is asigned to the temporary constant `tempVariable` and used within the code between the brackets.  
If it has no value, the code between the brackets is ignored.
```swift
if let tempVariable = optionalVariable {
    print("The value is \(tempVariable)"
}
```
