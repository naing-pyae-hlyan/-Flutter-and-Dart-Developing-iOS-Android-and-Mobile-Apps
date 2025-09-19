# Dart မှာ Variable နဲ့ Data Type များ

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Dart ဘာသာစကားမှာ variable နဲ့ data type တွေကို ပေါ့ပေါ့ပါးပါးနဲ့ ရှင်းပြပေးသွားမှာပါ။ App တစ်ခုတည်ဆောက်ဖို့အတွက် variable နဲ့ data type ကိုနားလည်ထားရင် အရမ်းအထောက်အကူဖြစ်ပါတယ်။

## Variable ဆိုတာဘာလဲ?
Variable တွေက data ကို သိမ်းထားဖို့ အသုံးပြုတဲ့ container လေးတွေပါ။ Variable တစ်ခုကို သုံးဖို့အတွက် အရင်ဆုံး variable ကို အမည်တစ်ခုနဲ့ ကြေညာရပါတယ်။ ပြီးရင် တန်ဖိုးတစ်ခု သတ်မှတ်ပေးရပါတယ်။

## Dart မှာ Variable ကြေညာနည်းများ
- **var:** Type ကို မသတ်မှတ်ဘဲ variable ကြေညာနိုင်တယ်။ Assign လုပ်တဲ့တန်ဖိုးအပေါ်မူတည်ပြီး type ကို Dart က ခန့်မှန်းပေးတယ်။
- **final:** တစ်ကြိမ်သာ တန်ဖိုးသတ်မှတ်နိုင်တယ်။ Runtime မှာတောင် assign လုပ်နိုင်တယ်။
- **const:** Compile-time မှာတန်ဖိုးသတ်မှတ်ပြီး ပြန်ပြောင်းလို့မရဘူး။

ဥပမာ -
```dart
var name = 'Aung Aung'; // ပြန်ပြောင်းနိုင်တယ်
final age = 20; // တစ်ကြိမ်သာ assign လုပ်နိုင်တယ်
const pi = 3.14; // တန်ဖိုးမပြောင်းနိုင်ဘူး
```

## Data Type များ
Dart က statically typed language ဖြစ်လို့ variable တစ်ခုချင်းစီမှာ data type ရှိပါတယ်။
- **int:** ကိန်းပြည့် (ဥပမာ - 10)
- **double:** ဒဿမကိန်း (ဥပမာ - 5.5)
- **String:** စာသား (ဥပမာ - 'Hello')
- **bool:** true/false တန်ဖိုး (ဥပမာ - true)
- **List:** အစီအစဉ်လိုက် data တွေ (ဥပမာ - [1,2,3])
- **Map:** key-value pair (ဥပမာ - {'name': 'Aung', 'age': 20})

## String Interpolation
String ထဲမှာ variable တန်ဖိုးထည့်ချင်ရင် `$variableName` သုံးနိုင်တယ်။
```dart
var name = 'Aung';
print('Hello $name'); // Output: Hello Aung
```

## List နဲ့ Map
- **List:** အစီအစဉ်လိုက် data တွေကို သိမ်းထားနိုင်တယ်။ Index 0 ကနေစတယ်။
- **Map:** key နဲ့ value တွေကို pair အနေနဲ့ သိမ်းထားတယ်။

## Null, Type Inference, Annotation
- **Null:** Variable တစ်ခုမှာ တန်ဖိုးမသတ်မှတ်ရင် null ဖြစ်နိုင်တယ်။ Nullable variable တွေကို `?` သုံးပြီး ကြေညာနိုင်တယ်။
- **Type Inference:** var သုံးရင် Dart က type ကို ခန့်မှန်းပေးတယ်။
- **Annotation:** Type ကို တိတိကျကျ ကြေညာချင်ရင် int, String စတဲ့ type ကို variable ကြေညာတဲ့အခါမှာ ထည့်နိုင်တယ်။

## အနှစ်ချုပ်
Variable တွေက data ကို သိမ်းထားဖို့ အသုံးပြုတယ်။ Dart မှာ variable ကြေညာဖို့ var, final, const သုံးနိုင်တယ်။ Data type တွေက int, double, String, bool, List, Map စသဖြင့် ရှိတယ်။ Null, type inference, annotation တွေကိုလည်း နားလည်ထားရင် code ကို ပိုမိုကောင်းကောင်း structure လုပ်နိုင်ပါတယ်။

