# Dart ဘာသာစကား အခြေခံများ 

ဒီအခန်းမှာတော့ Flutter app တည်ဆောက်ဖို့ အရေးကြီးတဲ့ Dart ဘာသာစကားရဲ့ အခြေခံအကြောင်းများကို လွယ်လွယ်ကူကူနဲ့ မြန်မာလို ရှင်းပြပေးပါမယ်။

## Dart ဆိုတာဘာလဲ၊ ဘာကြောင့် သုံးသင့်လဲ?
Dart က Google ဖန်တီးထားတဲ့ programming language တစ်ခုပါ။ Flutter app တွေကို တည်ဆောက်ဖို့ အဓိကသုံးပါတယ်။ Syntax လည်း လွယ်ကူပြီး performance မြန်မြန် app တွေ တည်ဆောက်နိုင်ပါတယ်။

## main() Function
Dart app တစ်ခုစတင် run တဲ့အချိန်မှာ main() function ကနေ စတင်တယ်။ ဥပမာ -
```dart
void main() {
  print('Hello World!');
}
```
main() function က app ရဲ့ starting point ဖြစ်ပြီး print() function က console မှာ စာသားတွေ output ပြတယ်။

## Variable & Data Types
Dart မှာ variable တွေက data ကိုသိမ်းထားဖို့ သုံးတယ်။
- var name = 'Flutter'; // Dart က type ကို auto ခန့်မှန်းတယ်
- int age = 30;
- double height = 5.9;
- String language = 'Dart';
- bool isAwesome = true;
- List<String> langs = ['Dart', 'JavaScript', 'Python'];

## Function
Function တွေက code ကို ပြန်သုံးနိုင်အောင် စုထားတာပါ။
```dart
void greet(String name) {
  print('Hello $name');
}

greet('Flutter'); // Output: Hello Flutter
```

## အကျဉ်းချုပ်
- Dart က Flutter app တွေတည်ဆောက်ဖို့ အဓိကသုံးတဲ့ language ပါ။
- main() function က app ရဲ့ starting point ဖြစ်တယ်။
- print() function က console မှာ output ပြတယ်။
- Variable, data type, function တွေကို နားလည်ထားရင် Flutter app တွေကို စတင်ရေးနိုင်ပြီ။

သင်တန်းသားအသစ်တွေအတွက် နားလည်ရလွယ်အောင် ရေးထားတာမလို့ သင့်အတွက် အထောက်အကူဖြစ်မယ်လို့ မျှော်လင့်ပါတယ်။
