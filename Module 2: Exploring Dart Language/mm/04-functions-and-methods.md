
# Dart မှာ Function နဲ့ Method များ

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Dart ဘာသာစကားမှာ function နဲ့ method တွေကို ပိုမိုရှင်းလင်းအောင်၊ နားလည်ရလွယ်အောင်၊ ပြန်သုံးနိုင်အောင် (reusable) နည်းလမ်းတွေနဲ့ ရှင်းပြပေးသွားမှာပါ။

## Function ဆိုတာဘာလဲ?
Function တွေက တစ်ခုတည်းသော အလုပ်တစ်ခုလုပ်ပေးတဲ့ reusable code block လေးတွေပါ။ Function တွေကို သုံးရင် code ကို ပြန်ပြန်သုံးနိုင်ပြီး၊ error နည်းနည်းနဲ့ စီမံခန့်ခွဲရလွယ်ပါတယ်။

### Function ကြေညာနည်း
```dart
void greet() {
	print('Hello World');
}

int add(int a, int b) {
	return a + b;
}

String sayHi(String name) {
	return 'Hi $name!';
}
```
main() function ကတော့ Dart app တစ်ခုစတင် run တဲ့နေရာပါ။

### Function ကို ဘယ်လိုခေါ်သုံးမလဲ?
```dart
greet();
print(add(2, 3)); // Output: 5
print(sayHi('Aung')); // Output: Hi Aung!
```

## Parameter မျိုးစုံ
- **Required parameter:** Function ကိုခေါ်တဲ့အခါ မဖြစ်မနေ ထည့်ရမယ့် parameter ပါ။
- **Optional parameter:** ထည့်မထည့် စိတ်ကြိုက်ပါ။
	- **Positional optional:** [ ] ထဲမှာရေးတယ်။
	- **Named optional:** { } ထဲမှာရေးတယ်။
- **Default value:** Parameter တစ်ခုကို default တန်ဖိုးပေးနိုင်တယ်။

ဥပမာ -
```dart
void greet(String name, [String? message]) {
	print('Hello $name, ${message ?? "How are you?"}');
}

void showInfo({required String name, int age = 18}) {
	print('$name is $age years old');
}

greet('Aung'); // Output: Hello Aung, How are you?
greet('Aung', 'Good morning!'); // Output: Hello Aung, Good morning!
showInfo(name: 'Mya'); // Output: Mya is 18 years old
showInfo(name: 'Mya', age: 25); // Output: Mya is 25 years old
```

## Arrow Function
Short function တွေကို `=>` သုံးပြီး ရေးနိုင်တယ်။
```dart
int square(int x) => x * x;
String greetShort(String name) => 'Hi $name!';
```

## Function Return Type
Function တစ်ခုက return type မရှိရင် void သုံးတယ်။ Return type ရှိရင် int, String စသဖြင့် သတ်မှတ်နိုင်တယ်။

## Function ကို ပြန်သုံးနိုင်အောင် (Reusable) ရေးနည်း
- Function တစ်ခုတည်းကို parameter မျိုးစုံနဲ့ ခေါ်သုံးနိုင်အောင်ရေးပါ။
- Function တစ်ခုမှာ တစ်ခုတည်းသော အလုပ်တစ်ခုသာ လုပ်ပါစေ။
- Function name ကို ရိုးရှင်းရှင်းနဲ့ အလုပ်အရည်အချင်းကိုဖော်ပြအောင် နာမည်ပေးပါ။

ဥပမာ -
```dart
double calculateArea(double width, double height) {
	return width * height;
}

print(calculateArea(5, 10)); // Output: 50
```

## Method ဆိုတာဘာလဲ?
Method တွေက class ထဲမှာရေးတဲ့ function တွေပါ။ Object တစ်ခုရဲ့ data တွေကို ကိုင်တွယ်ဖို့ သုံးတယ်။
```dart
class Person {
	String name;
	Person(this.name);
	void sayHello() {
		print('Hello $name');
	}
	int nameLength() => name.length;
}

var p = Person('Aung');
p.sayHello(); // Output: Hello Aung
print(p.nameLength()); // Output: 4
```

## Closure ဆိုတာဘာလဲ?
Closure ဆိုတာ function တစ်ခုက သူ့ကိုဖန်တီးတဲ့ scope ထဲက variable တွေကို သိမ်းထားနိုင်တာပါ။
```dart
Function makeAdder(int addBy) {
	return (int i) => addBy + i;
}
var add2 = makeAdder(2);
print(add2(3)); // Output: 5
```

## Best Practices & Tips
- Function တွေကို code duplication မဖြစ်အောင် ပြန်သုံးနိုင်အောင်ရေးပါ။
- Function တစ်ခုမှာ တစ်ခုတည်းသော အလုပ်သာ လုပ်ပါစေ။
- Parameter များစွာလိုအပ်ရင် named parameter သုံးပါ။
- Function ကို documentation comment (///) နဲ့ ရှင်းပြပေးပါ။

```dart
/// Add two numbers and return the result.
int add(int a, int b) => a + b;
```

## အနှစ်ချုပ်
Function တွေက reusable code block လေးတွေပါ။ Parameter မျိုးစုံ၊ default value, arrow function, method, closure, best practice စတဲ့ concept တွေကို နားလည်ထားရင် Dart code ကို ပိုမိုပြည့်စုံစွာ ရေးနိုင်ပါတယ်။