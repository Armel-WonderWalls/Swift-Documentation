# Swift Documentation
## What is Swift?
Swift is the language developed by Apple to replace Objective-C which was criticized for being hard to learn and had weird syntax.  
It's advertised as "fast, modern, safe and interactive".
### Objective-C
```objective-c
const int count = 10;
double price = 23.55;

NSString *firstMessage = @"Swift is awesome. ";
NSString *secondMessage = @"What do you think?";
NSString *message = [NSString stringWithFormat:@"%@%@", firstMessage, secondMessage];

NSLog(@"%@", message);
```
### Swift
```swift
let count = 10
var price = 23.55

let firstMessage = "Swift is awesome. "
let secondMessage = "What do you think?"
var message = firstMessage + secondMessage

print(message)
```