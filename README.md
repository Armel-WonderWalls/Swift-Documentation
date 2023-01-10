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
