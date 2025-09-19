# Dart မှာ Class များ

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Dart ဘာသာစကားမှာ class, object, getter, setter, encapsulation, inheritance စတဲ့ OOP (Object-Oriented Programming) အကြောင်းအရာတွေကို ပေါ့ပေါ့ပါးပါးနဲ့ ရှင်းပြပေးသွားမှာပါ။

## Class နဲ့ Object ဆိုတာဘာလဲ?
Class ကတော့ object တစ်ခုဖန်တီးဖို့အတွက် blueprint (ပုံစံ) တစ်ခုပါ။ Object တွေကတော့ class ကိုအခြေခံပြီး ဖန်တီးထားတဲ့ တကယ့်အသုံးပြုနိုင်တဲ့ data တွေပါ။

```dart
class Person {
  String name;
  int age;
  Person(this.name, this.age);
  void sayHello() {
    print('Hello, my name is $name.');
  }
}

var p = Person('Aung', 20);
p.sayHello(); // Output: Hello, my name is Aung.
```

## Public နဲ့ Private Property
- Public property တွေက class အပြင်မှာတောင် အသုံးပြုနိုင်တယ်။
- Private property တွေက class အတွင်းမှာပဲ အသုံးပြုနိုင်တယ်။ Dart မှာ `_` (underscore) သုံးရင် private ဖြစ်တယ်။

```dart
class BankAccount {
  String _accountNumber;
  double _balance;
  BankAccount(this._accountNumber, this._balance);
  double get balance => _balance;
  set deposit(double amount) {
    if (amount > 0) _balance += amount;
  }
  void withdraw(double amount) {
    if (amount <= _balance) _balance -= amount;
  }
}
```

## Method, Getter, Setter
- Method တွေက object ရဲ့ အပြုအမူ (behavior) ကိုဖော်ပြတယ်။
- Getter က property တစ်ခုရဲ့ တန်ဖိုးကို ရယူဖို့၊ setter က property တစ်ခုကို ပြင်ဖို့ အသုံးပြုတယ်။

```dart
class Rectangle {
  double _width, _height;
  Rectangle(this._width, this._height);
  double get area => _width * _height;
  set width(double w) {
    if (w > 0) _width = w;
  }
}
```

## Static Method
Static method တွေက object instance မလိုဘဲ class name နဲ့ ခေါ်သုံးနိုင်တယ်။ Utility function တွေအတွက် အသုံးများတယ်။

```dart
class MathUtil {
  static double pi = 3.14;
  static double square(double x) => x * x;
}
print(MathUtil.square(5)); // Output: 25
```

## Anonymous Function (Lambda)
Anonymous function တွေက နာမည်မဲ့ function တွေပါ။

```dart
var numbers = [1, 2, 3];
numbers.forEach((n) => print(n));
```

## Encapsulation
Encapsulation ဆိုတာ object ရဲ့ sensitive data တွေကို private property နဲ့ ကာကွယ်ပြီး getter, setter နဲ့ပဲ ပြင်နိုင်အောင်လုပ်တာပါ။

## Inheritance
Inheritance ဆိုတာ class တစ်ခုကနေ property, method တွေကို အမွေခံအဖြစ် ဆက်ခံရတဲ့ OOP concept ပါ။

```dart
class Animal {
  void eat() => print('Eating');
}
class Dog extends Animal {
  void bark() => print('Woof!');
}
var d = Dog();
d.eat(); // Output: Eating
d.bark(); // Output: Woof!
```

## အနှစ်ချုပ်
Class တွေက object တွေဖန်တီးဖို့ blueprint ဖြစ်တယ်။ Public/private property, getter/setter, static method, anonymous function, encapsulation, inheritance စတဲ့ OOP concept တွေကို နားလည်ထားရင် Dart နဲ့ complex app တွေကို structure ကောင်းကောင်းနဲ့ တည်ဆောက်နိုင်ပါတယ်။
