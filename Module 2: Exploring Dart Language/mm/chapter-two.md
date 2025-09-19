
# အခန်း (၂) – Dart Programming Language ကို လေ့လာခြင်း (အပြည့်အစုံ)

ဒီအခန်းမှာ Dart programming language ၏ အခြေခံအကြောင်းအရာများ၊ syntax, data types, functions, classes, libraries, command-line, cheat sheet, troubleshooting, best practices, quizzes, exercises စသည်တို့ကို မြန်မာလို ရှင်းလင်းပြောပြပေးထားပါတယ်။ နမူနာ code များ၊ step-by-step guide များ၊ အကြောင်းအရာများစွာပါဝင်သဖြင့် စတင်လေ့လာသူများအတွက် အလွယ်တကူနားလည်နိုင်ပါသည်။

---

## ၁။ Dart ဆိုတာဘာလဲ?
Dart သည် Google မှ ဖန်တီးထားသော object-oriented, strongly typed, UI development အတွက် အထူးသင့်တော်သော programming language ဖြစ်သည်။

**Dart ၏ အားသာချက်များ**
- Syntax ရိုးရှင်းလွယ်ကူသည်
- Null safety ပါဝင်သည်
- Fast compilation (JIT & AOT)
- Web, Mobile, Desktop, Server အတွက် အသုံးပြုနိုင်သည်
- Flutter ၏ အခြေခံဘာသာစကား

**Dart ကို ဘာကြောင့် သုံးသင့်သလဲ?**
- UI development အတွက် အထူးသင့်တော်သည်
- Learning curve နိမ့်သည်
- Community support ကြီးမားသည်

---

## ၂။ Dart Syntax & Fundamentals

### ၂.၁ Syntax Basics
- Semicolon (;) ဖြင့် statement ပြီးဆုံးသည်
- Curly braces ({}) ဖြင့် code block သတ်မှတ်သည်
- //, /* */ ဖြင့် comment ရေးနိုင်သည်

**နမူနာ**
```dart
void main() {
	print('Hello, Dart!');
}
```

### ၂.၂ Variables & Types
Dart သည် strongly typed ဖြစ်သော်လည်း `var` ဖြင့် type inference ပြုလုပ်နိုင်သည်။

**Data Types နမူနာ**
```dart
int age = 20;
double price = 9.99;
String name = 'Dart';
bool isActive = true;
List<int> numbers = [1, 2, 3];
Map<String, int> scores = {'Alice': 90, 'Bob': 85};
Set<String> fruits = {'apple', 'banana'};
```

**Variables & Constants**
```dart
var city = 'Yangon'; // type inference
final country = 'Myanmar'; // value set once
const pi = 3.14159; // compile-time constant
```

### ၂.၃ Operators
```dart
int a = 10, b = 3;
print(a + b); // 13
print(a - b); // 7
print(a * b); // 30
print(a / b); // 3.333...
print(a ~/ b); // 3 (integer division)
print(a % b); // 1
```

### ၂.၄ Control Flow
```dart
if (age > 18) {
	print('Adult');
} else {
	print('Minor');
}
for (var fruit in fruits) {
	print(fruit);
}
while (age < 25) {
	age++;
}
```

### ၂.၅ Functions & Methods
Function များသည် reusable code blocks ဖြစ်သည်။ Method များသည် class အတွင်းရှိ function များဖြစ်သည်။

**နမူနာ**
```dart
int add(int a, int b) {
	return a + b;
}

int multiply(int a, int b) => a * b;

void greet(String name) {
	print('Hello, $name!');
}
```

**Optional & Named Parameters**
```dart
void printInfo(String name, {int age = 18}) {
	print('Name: $name, Age: $age');
}
printInfo('Aung Aung'); // Name: Aung Aung, Age: 18
printInfo('Mg Mg', age: 25); // Name: Mg Mg, Age: 25
```

---

## ၃။ Classes & Object-Oriented Programming

Dart သည် object-oriented ဖြစ်သဖြင့် class များကို အသုံးပြုသည်။

**Class နမူနာ**
```dart
class Person {
	String name;
	int age;
	Person(this.name, this.age);
	void greet() {
		print('Hello, my name is $name.');
	}
}

void main() {
	var p = Person('Aung Aung', 20);
	p.greet();
}
```

**Inheritance (အမွေဆက်ခံခြင်း)**
```dart
class Animal {
	void eat() => print('Eating');
}
class Dog extends Animal {
	void bark() => print('Woof!');
}
```

**Abstract Classes & Interfaces**
```dart
abstract class Shape {
	double area();
}
class Circle extends Shape {
	double radius;
	Circle(this.radius);
	@override
	double area() => 3.14 * radius * radius;
}
```

**Mixins**
```dart
mixin Swimmer {
	void swim() => print('Swimming');
}
class Fish with Swimmer {}
```

---

## ၄။ Libraries & Packages

Dart တွင် built-in libraries များရှိပြီး ကိုယ်ပိုင် library များလည်း ဖန်တီးနိုင်သည်။

**Import နမူနာ**
```dart
import 'dart:math';
import 'package:http/http.dart' as http;
```

**Library ဖန်တီးနည်း**
```dart
// lib/utils.dart
String capitalize(String s) => s[0].toUpperCase() + s.substring(1);
```

---

## ၅။ Error Handling

**Try-Catch-Finally**
```dart
try {
	int result = 10 ~/ 0;
} catch (e) {
	print('Error: $e');
} finally {
	print('Done');
}
```

**Custom Exceptions**
```dart
class CustomException implements Exception {
	final String message;
	CustomException(this.message);
	String toString() => 'CustomException: $message';
}

void test() {
	throw CustomException('Something went wrong');
}
```

---

## ၆။ Command-Line & Utilities

Dart ကို command-line script များအတွက်လည်း အသုံးပြုနိုင်သည်။

**Run Script နမူနာ**
```sh
dart run my_script.dart
```

**Command-Line Arguments**
```dart
void main(List<String> args) {
	print('Arguments: $args');
}
```

---

## ၇။ Null Safety

Dart ၏ null safety feature သည် null-related bugs များကို ကာကွယ်ပေးသည်။

```dart
String? name; // nullable
name = null;
String nonNull = 'Hello';
// nonNull = null; // error
```

---

## ၈။ Summary & Highlights
- Dart သည် Flutter ၏ အခြေခံဘာသာစကားဖြစ်သည်
- Syntax ရိုးရှင်းလွယ်ကူသည်
- Data types, functions, classes, libraries, command-line, error handling, null safety စသည်တို့ကို နားလည်ထားပါ

---

## ၉။ Cheat Sheet
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

## ၁၀။ Quiz & Exercises

### Quiz
1. Dart ၏ အားသာချက်တစ်ခုမှာ?
2. Null safety ဆိုတာဘာလဲ?
3. Dart မှာ class ကို ဘယ်လိုရေးသလဲ?
4. Function နမူနာတစ်ခုရေးပါ။
5. Error handling ကို ဘယ်လိုလုပ်သလဲ?

### Exercises
1. Person class ကိုရေးပါ။
2. List, Map, Set ကို အသုံးပြုပြီး data structure တစ်ခုရေးပါ။
3. Custom exception တစ်ခုရေးပါ။
4. Command-line arguments ကို အသုံးပြုပြီး script တစ်ခုရေးပါ။

---

## ၁၁။ Troubleshooting & Best Practices

- Variable type မမှန်လျှင် error ဖြစ်နိုင်သည်
- Null safety ကို သတိပြုပါ
- pubspec.yaml မှာ dependency version conflict ဖြစ်နိုင်သည်
- Code ကို function/class အလိုက် ခွဲရေးပါ
- Dart documentation ကို အမြဲလေ့လာပါ

---

## ၁၂။ Glossary (အဓိပ္ပါယ်ရှင်းလင်းချက်များ)

| Term | Definition |
|------|------------|
| Null safety | Null-related bugs ကို ကာကွယ်ပေးသော feature |
| Exception | Error handling mechanism |
| Mixin | Class တစ်ခုထက်ပို၍ extend လုပ်နိုင်စေသော syntax |
| Library | Code reuse အတွက် module |
| Package | Reusable code bundle |
| ... | ... |

---

## ၁၃။ အကျဉ်းချုပ်
- Dart သည် modern, safe, productive programming language တစ်ခုဖြစ်သည်။
- Flutter app development အတွက် အခြေခံအရင်းအမြစ်ဖြစ်သည်။

---

အခန်း (၂) ကို ပြီးဆုံးပါပြီ။ နောက်ထပ်အခန်းများတွင် Dart ကို Flutter app တွင် အသုံးချနည်းများကို ဆက်လက်လေ့လာနိုင်ပါသည်။
