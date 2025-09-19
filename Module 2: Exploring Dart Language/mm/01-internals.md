# Dart ဘာသာစကားရဲ့ အတွင်းပိုင်း (Internals of Dart)

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Dart ဘာသာစကားရဲ့ အရေးကြီးတဲ့ အတွင်းပိုင်းအကြောင်းတွေကို ပေါ့ပေါ့ပါးပါးနဲ့ ရှင်းပြပေးသွားမှာပါ။ Flutter app တွေတည်ဆောက်ဖို့ Dart ကိုသိထားရင် အရမ်းအထောက်အကူဖြစ်မှာပါ။

## Dart VM (Virtual Machine) ဆိုတာဘာလဲ?
Dart VM ကတော့ Dart code တွေကို run ပေးတဲ့ engine တစ်ခုပါ။ Memory ကိုစီမံပေးတာ၊ code ကို run ပေးတာတွေကို ကိုင်တွယ်ပေးပါတယ်။

## Compile-time နဲ့ Run-time
Dart မှာ code တွေကို compile-time (ရေးနေချိန်) မှာ error တွေစစ်ပေးတယ်။ Run-time (app ကို run နေချိန်) မှာတော့ Dart VM က code ကို run ပေးပါတယ်။ ဒါကြောင့် app တွေ မြန်မြန်ဆန်ဆန်နဲ့ error နည်းနည်းနဲ့ ရရှိနိုင်ပါတယ်။

## JIT နဲ့ AOT Compilation
- **JIT (Just-In-Time):** App ကို run နေချိန်မှာ code ကို machine code အဖြစ် ပြောင်းပေးတယ်။ Development အတွက် အရမ်းအသုံးဝင်ပြီး hot reload feature ကို အသုံးပြုနိုင်ပါတယ်။
- **AOT (Ahead-Of-Time):** App ကို run မလုပ်ခင်မှာ code အားလုံးကို machine code အဖြစ် ပြောင်းပေးတယ်။ App ကို startup မြန်မြန်နဲ့ run ပေးနိုင်ပါတယ်။

## Garbage Collection (Memory စီမံမှု)
Dart မှာ garbage collection ဆိုတာက memory ကို အလိုအလျောက် သန့်ရှင်းပေးတာပါ။ အသုံးမလိုတော့တဲ့ data တွေကို ဖယ်ရှားပေးပါတယ်။
- **Young Generation:** တစ်ချိန်တည်းမှာ အသုံးပြုပြီး ပြီးသွားတဲ့ object တွေ။ (ဥပမာ - ဖတ်ပြီးသား message တွေ)
- **Old Generation:** အမြဲတမ်းအသုံးပြုနေတဲ့ object တွေ။ (ဥပမာ - contact list)

## Concurrency (အချိန်တစ်ပြိုင်နက်လုပ်ဆောင်နိုင်မှု)
Dart မှာ isolate နဲ့ async programming ကိုသုံးပြီး တစ်ပြိုင်နက်တည်း အလုပ်များများလုပ်နိုင်ပါတယ်။
- **Isolate:** Memory မမျှဝေဘဲ တစ်ခုချင်းစီ သီးသန့်အလုပ်လုပ်နိုင်တဲ့ worker တွေပါ။ Message ပို့ပြီး ဆက်သွယ်ကြတယ်။
- **Async/await:** Data load တာ၊ file ဖတ်တာလို အချိန်ကြာတဲ့အလုပ်တွေကို app မရပ်ဘဲ နောက်ကွယ်မှာလုပ်နိုင်ပါတယ်။

ဥပမာ - App တစ်ခုမှာ web server ကနေ data load လုပ်ရင် user ကို စောင့်နေရစေမယ့်အစား background မှာ data ကို load လုပ်ပြီး ပြီးရင် UI ကို update လုပ်ပေးနိုင်ပါတယ်။

## Dart Core Libraries
Dart မှာ အသုံးများတဲ့ library တွေပါဝင်ပါတယ်။
- **dart:core:** Number, String, List စတဲ့ အခြေခံ class တွေပါဝင်တယ်။
- **dart:async:** Future, Stream စတဲ့ async programming အတွက် class တွေပါဝင်တယ်။
- **dart:io:** File ဖတ်/ရေး၊ internet ချိတ်ဆက်တာတွေအတွက် အသုံးဝင်တယ်။
- **dart:convert:** JSON data ကို Dart object ပြောင်းတာ၊ ပြန်ပြောင်းတာတွေအတွက် အသုံးဝင်တယ်။
- **dart:math:** Math function တွေ၊ constant တွေပါဝင်တယ်။

## အနှစ်ချုပ်
Dart VM, JIT/AOT compilation, garbage collection, concurrency နဲ့ core libraries တွေကြောင့် Dart က cross-platform app တွေတည်ဆောက်ဖို့ အရမ်းသင့်တော်ပါတယ်။ ဒီအချက်တွေကို နားလည်ထားရင် Flutter နဲ့ Dart ကို ပိုမိုအောင်မြင်စွာ အသုံးချနိုင်ပါပြီ။
