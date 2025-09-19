
# Cheat Sheet: Exploring Dart Language

## Variables and Types
| Type    | Description                    | Code Example                       |
|---------|--------------------------------|------------------------------------|
| Var     | Inferred type variable         | `var name = 'Dart';`               |
| Dynamic | Variable types can change      | `dynamic x = 42;`                  |
| Final   | Constant at runtime            | `final cityName = 'New York';`     |
| Const   | Compile-time constant          | `const PI = 3.14;`                 |

## Functions and Methods
| Type                        | Description                                              | Code Example                                                      |
|-----------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Function                    | Defines a function that adds two numbers                 | `int add(int a, int b) => a + b;`                                |
| Arrow syntax                | Concise function declaration                             | `void printItem(item) => print(item);`                           |
| Required parameters         | Must be provided in the function call                    | `int multiply(int a, int b) => a * b;`                           |
| Optional positional params  | Can be omitted; use square brackets                      | `String fullName(String first, [String mid, String last])`        |
| Named parameters            | Specified by name; curly braces, can be required/default | `void greet({required String name, String greeting = 'Hello'}) => print('$greeting, $name!');` |
| Default parameters          | Allows default values if not provided                    | `String describe(String name, {int age = 30, String city = 'Unknown'})` |
| Closures                    | Anonymous functions capturing variables                  | `numbers.forEach((n) => print(n * 2));`                          |

## Classes and OOP
| Type              | Description                                   | Code Example                                  |
|-------------------|-----------------------------------------------|-----------------------------------------------|
| Class             | Defines a class with properties               | `class Person { String name; int age; }`      |
| Inheritance       | Basic inheritance in Dart                     | `class Employee extends Person { int salary; }`|
| Encapsulation     | Methods/visibility to enforce encapsulation   | `class Person { String name; int _age; }`     |
| Public properties | Can be accessed from anywhere                 | `class Person { String name; }`               |
| Private properties| Only accessed within the class (underscore)   | `class Person { int _age; }`                  |
| Getters/Setters   | Control access to class properties            | `class Person { int _age; int get age => _age; set age(int v) { _age = v; } }` |
| Static methods    | Belong to class, called without object        | `class Utility { static int add(int a, int b) => a + b; }` |
| Anonymous functions| Single-expression functions (lambdas)        | `list.forEach((item) { print(item); });`      |

## Common Data Structures
| Type      | Description                        | Code Example                                 |
|-----------|------------------------------------|----------------------------------------------|
| List      | Ordered collection of items        | `List<int> numbers = [1, 2, 3];`             |
| Map       | Key-value pairs collection         | `Map<String, int> ages = {'Alice': 18, 'Bob': 20};` |
| Set       | Unordered collection of unique     | `Set<String> names = {'Alice', 'Bob'};`      |
| Queues    | FIFO collection for elements       | `Queue<int> queue = Queue(); queue.addAll([1,2,3]);` |
| LinkedList| Sequence where each points to next | `LinkedList<int> linkedList = LinkedList(); linkedList.add(1);` |

## Libraries and Command Line Utilities
| Type         | Description                                 | Code Example                                 |
|--------------|---------------------------------------------|----------------------------------------------|
| Import       | Access built-in Dart libraries               | `import 'dart:math';`                        |
| CLI commands | Compile Dart code to native executable       | `dart compile exe test.dart`                 |
| Dart SDK     | Tool for running/managing Dart apps          | `dart run`, `dart create`                    |
| Pub tool     | Package manager for dependencies             | `dart pub get`, `dart pub add http`          |
| Dart DevTools| Debugging and performance profiling suite     | Performance profiling, memory analysis, widget inspection |
| dart:core    | Fundamental classes and functions            | Handling strings, numbers, List, Map         |
| dart:math    | Math constants and functions                 | `sin`, `cos`, `sqrt`, `pi`                   |
| dart:async   | Asynchronous programming support             | `Future`, `Stream`                           |
| dart:convert | JSON, UTF-8 encoding/decoding                | `jsonEncode`, `jsonDecode`                   |
| Custom libs  | Creating and using your own library          | `library my_utils; int add(int a, int b) => a + b;` |