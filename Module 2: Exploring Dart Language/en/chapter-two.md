# Chapter Two: Exploring Dart Language

Welcome to Chapter Two! This chapter brings together all the essential topics from Module 2, making it easy for beginners to understand Dart—the language behind Flutter. Each section is simplified for clarity and practical learning, with simple examples.

---

## 1. Dart Internals
Dart is an open-source, object-oriented programming language developed by Google. It is designed for building fast, modern apps for mobile, web, and desktop. Dart compiles to native code for high performance and is optimized for UI development.

---

## 2. Dart Fundamentals
Dart’s syntax is easy to learn, especially if you know JavaScript, Java, or C#.

```dart
void main() {
  print('Hello, Dart!');
}
```

---

## 3. Variables and Types
Variables store data. Dart is strongly typed, but you can use `var` for type inference.

**Common Types:**
- `int`: Whole numbers
- `double`: Decimal numbers
- `String`: Text
- `bool`: true or false
- `List`: Ordered collection (array)
- `Map`: Key-value pairs
- `Set`: Unique items

```dart
int age = 20;
double price = 9.99;
String name = 'Dart';
bool isActive = true;
List<int> numbers = [1, 2, 3];
Map<String, int> scores = {'Alice': 90, 'Bob': 85};
Set<String> fruits = {'apple', 'banana'};
```

---

## 4. Functions and Methods
Functions are reusable blocks of code. Methods are functions inside classes.

```dart
int add(int a, int b) {
  return a + b;
}

int multiply(int a, int b) => a * b;
```

---

## 5. Classes
Dart is object-oriented. Classes are blueprints for objects.

```dart
class Person {
  String name;
  int age;

  Person(this.name, this.age);

  void greet() {
    print('Hello, my name is $name.');
  }
}
```

---

## 6. Libraries
Libraries help organize code and reuse functionality. Dart has built-in libraries (like `dart:core`, `dart:math`) and you can create your own.

```dart
import 'dart:math';
```

---

## 7. Command-Line and Utilities
Dart can be used for command-line scripts and utilities, not just Flutter apps.

```sh
dart run my_script.dart
```

---

## 8. Summary and Highlights
- Dart is the language behind Flutter
- It’s easy to learn and optimized for UI
- Strongly typed, object-oriented, and fast
- Supports functions, classes, and libraries
- Can be used for both apps and scripts

---

## 9. Dart Cheat Sheet

```dart
var name = 'Dart';
final age = 20;
const pi = 3.14;

String greet(String name) => 'Hello, $name!';

class Car {
  String model;
  Car(this.model);
}

List<String> fruits = ['apple', 'banana'];

if (age > 18) {
  print('Adult');
} else {
  print('Minor');
}

for (var fruit in fruits) {
  print(fruit);
}
```

---

Congratulations! You’ve completed Chapter Two. You now have a solid understanding of Dart fundamentals. Continue to the next chapter to apply these skills in real Flutter projects!
