# Cheat Sheet: Dart ဘာသာစကား (မြန်မာ)

## Variable နဲ့ Type များ
| Type    | ဖော်ပြချက်                        | နမူနာကုဒ်                       |
|---------|------------------------------------|------------------------------------|
| Var     | Type ကို auto ခန့်မှန်း variable   | `var name = 'Dart';`               |
| Dynamic | Type ပြောင်းလဲနိုင်တဲ့ variable   | `dynamic x = 42;`                  |
| Final   | Runtime မှာတန်ဖိုးမပြောင်းနိုင်     | `final cityName = 'New York';`     |
| Const   | Compile-time မှာတန်ဖိုးမပြောင်းနိုင်| `const PI = 3.14;`                 |

## Function နဲ့ Method များ
| Type                        | ဖော်ပြချက်                                              | နမူနာကုဒ်                                                      |
|-----------------------------|--------------------------------------------------------|-------------------------------------------------------------------|
| Function                    | နံပါတ် ၂ ခုပေါင်းတဲ့ function                        | `int add(int a, int b) => a + b;`                                |
| Arrow syntax                | တစ်ကြောင်း function ရေးနည်း                           | `void printItem(item) => print(item);`                           |
| Required parameters         | မဖြစ်မနေထည့်ရမယ့် parameter                           | `int multiply(int a, int b) => a * b;`                           |
| Optional positional params  | မထည့်လည်းရတဲ့ parameter ([ ])                         | `String fullName(String first, [String mid, String last])`        |
| Named parameters            | နာမည်နဲ့ခေါ်တဲ့ parameter ({ })                       | `void greet({required String name, String greeting = 'Hello'}) => print('$greeting, $name!');` |
| Default parameters          | Default တန်ဖိုးပါ parameter                            | `String describe(String name, {int age = 30, String city = 'Unknown'})` |
| Closures                    | Context ထဲက variable တွေသိမ်းထားနိုင်တဲ့ function      | `numbers.forEach((n) => print(n * 2));`                          |

## Class နဲ့ OOP
| Type              | ဖော်ပြချက်                                   | နမူနာကုဒ်                                  |
|-------------------|---------------------------------------------|-----------------------------------------------|
| Class             | Property ပါတဲ့ class တစ်ခုရေးနည်း          | `class Person { String name; int age; }`      |
| Inheritance       | မိဘ class ကနေ ဆက်ခံရေးနည်း                | `class Employee extends Person { int salary; }`|
| Encapsulation     | Method/visibility နဲ့ data ကာကွယ်ရေးနည်း     | `class Person { String name; int _age; }`     |
| Public properties | အပြင်မှာ access လုပ်လို့ရတဲ့ property       | `class Person { String name; }`               |
| Private properties| class အတွင်းမှာပဲ access လုပ်လို့ရတဲ့ property| `class Person { int _age; }`                  |
| Getters/Setters   | Property ကို getter/setter နဲ့ထိန်းချုပ်      | `class Person { int _age; int get age => _age; set age(int v) { _age = v; } }` |
| Static methods    | Object မလိုဘဲ class နဲ့ခေါ်နိုင်တဲ့ method   | `class Utility { static int add(int a, int b) => a + b; }` |
| Anonymous functions| တစ်ကြောင်း function (lambda)                | `list.forEach((item) { print(item); });`      |

## Data Structure များ
| Type      | ဖော်ပြချက်                        | နမူနာကုဒ်                                 |
|-----------|------------------------------------|----------------------------------------------|
| List      | အစီအစဉ်လိုက် data တွေ           | `List<int> numbers = [1, 2, 3];`             |
| Map       | key-value pair collection          | `Map<String, int> ages = {'Alice': 18, 'Bob': 20};` |
| Set       | ထပ်မကျတဲ့ data တွေစု              | `Set<String> names = {'Alice', 'Bob'};`      |
| Queues    | FIFO (အရင်ဝင်-အရင်ထွက်)           | `Queue<int> queue = Queue(); queue.addAll([1,2,3]);` |
| LinkedList| တစ်ခုနောက်တစ်ခုချိတ်တဲ့ data      | `LinkedList<int> linkedList = LinkedList(); linkedList.add(1);` |

## Library နဲ့ Command Line Tool များ
| Type         | ဖော်ပြချက်                                 | နမူနာကုဒ်                                 |
|--------------|-------------------------------------------|----------------------------------------------|
| Import       | Built-in Dart library ကို import           | `import 'dart:math';`                        |
| CLI commands | Dart code ကို native executable ပြောင်း    | `dart compile exe test.dart`                 |
| Dart SDK     | Dart app run/manage လုပ်ဖို့ tool          | `dart run`, `dart create`                    |
| Pub tool     | Dependency စီမံဖို့ package manager        | `dart pub get`, `dart pub add http`          |
| Dart DevTools| Debug/performance profiling tool suite      | Performance profiling, memory analysis, widget inspection |
| dart:core    | အခြေခံ class/function တွေ                  | String, number, List, Map ကို ကိုင်တွယ်နိုင်တယ် |
| dart:math    | Math function/constant တွေ                  | `sin`, `cos`, `sqrt`, `pi`                   |
| dart:async   | Async programming အတွက် support             | `Future`, `Stream`                           |
| dart:convert | JSON, UTF-8 encode/decode                   | `jsonEncode`, `jsonDecode`                   |
| Custom libs  | ကိုယ်ပိုင် library ဖန်တီး/သုံးနည်း           | `library my_utils; int add(int a, int b) => a + b;` |
