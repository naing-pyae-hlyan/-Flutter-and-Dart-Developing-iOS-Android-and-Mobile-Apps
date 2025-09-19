# Dart ဘာသာစကားရဲ့ အခြေခံအကြောင်းအရာများ

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Dart ဘာသာစကားရဲ့ အခြေခံအကြောင်းအရာတွေကို ပေါ့ပေါ့ပါးပါးနဲ့ ရှင်းပြပေးသွားမှာပါ။ Flutter app တွေတည်ဆောက်ဖို့ Dart ကိုနားလည်ထားရင် အရမ်းအထောက်အကူဖြစ်မှာပါ။

## Dart ကို Flutter မှာ ဘာကြောင့်သုံးလဲ?
Dart က Google ဖန်တီးထားတဲ့ modern programming language တစ်ခုပါ။ Flutter app တွေကို cross-platform အနေနဲ့ မြန်မြန် compile လုပ်နိုင်တယ်။ UI ကို reactive programming နဲ့ တည်ဆောက်နိုင်လို့ app တွေ မြန်မြန်နဲ့ smooth ဖြစ်တယ်။ Hot reload feature ပါဝင်လို့ code ပြင်တာနဲ့ UI ကို ချက်ချင်းမြင်နိုင်တယ်။ Syntax က JavaScript နဲ့ဆင်တူလို့ သင်ယူရလွယ်ကူတယ်။

## Dart ရဲ့ အခြေခံအကြောင်းအရာများ
- **Everything is an object:** Variable ထဲထည့်နိုင်တဲ့အရာတိုင်းက object တစ်ခုပါ။ Number, function, null တို့ပါဝင်တယ်။ Null safety ကို enable လုပ်ထားရင် variable တစ်ခုကို nullable (null ဖြစ်နိုင်) လုပ်နိုင်တယ်။
- **Variables, operators, functions, classes:** App တစ်ခုတည်ဆောက်ဖို့ အဓိကအကြောင်းအရာတွေပါ။ Object-oriented programming ကို support လုပ်လို့ class, object တွေသုံးပြီး code ကို structure ကောင်းကောင်းနဲ့ ရေးနိုင်တယ်။
- **Async programming:** Network request, data load တို့လို အချိန်ကြာတဲ့အလုပ်တွေကို Future, Stream နဲ့ handle လုပ်နိုင်တယ်။

## Iterable, Iterator, Collection ဆိုတာဘာလဲ?
- **Collection:** Object တွေစုထားတဲ့ group တစ်ခုပါ။ (ဥပမာ - List, Set, Map)
- **Iterable:** Collection ထဲက element တွေကို အစဉ်လိုက် access လုပ်နိုင်တဲ့အရာပါ။
- **Iterator:** Iterable ထဲက element တစ်ခုချင်းစီကို順လိုက်ယူနိုင်တဲ့ interface ပါ။

ဥပမာ - List<int> ဆိုတာက iterable collection တစ်ခုပါ။ Iterator သုံးပြီး element တစ်ခုချင်းစီကို loop နဲ့ယူနိုင်တယ်။

## Flutter App တွေမှာ ဘာလို့ အရေးကြီးလဲ?
Collection, iterable, iterator တွေကို data တွေကို UI မှာ ပြသဖို့၊ စီမံဖို့ အရမ်းအသုံးဝင်တယ်။ ဥပမာ - chat app မှာ message list, e-commerce app မှာ item list တို့လို data တွေကို လွယ်လွယ်ကူကူ ပြသနိုင်တယ်။

## အနှစ်ချုပ်
Dart ရဲ့ object-oriented, async programming, collection, iterable, iterator concept တွေကို နားလည်ထားရင် Flutter app တွေကို structure ကောင်းကောင်းနဲ့ မြန်မြန်ဆန်ဆန် တည်ဆောက်နိုင်ပါတယ်။
