# Flutter App ရေးဖို့အတွက် Development Environment

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Flutter app တစ်ခုတည်ဆောက်ဖို့အတွက် ဘာတွေလိုအပ်လဲ၊ ဘယ်လို tool တွေသုံးရမလဲဆိုတာကို ပေါ့ပေါ့ပါးပါးနဲ့ ရှင်းပြပေးသွားမှာပါ။

## Flutter Development Environment မှာ ဘာတွေပါလဲ?

- **Flutter SDK:** App ရေးဖို့အတွက် လိုအပ်တဲ့ လက်နက်ကိရိယာတွေ စုထားတဲ့ သေတ္တာတစ်လုံးလိုပါပဲ။ သူ့ထဲမှာ Dart SDK လည်း ပါပြီးသားပါ။
- **Dart Programming Language:** Flutter app တွေရေးဖို့အတွက် အသုံးပြုရမယ့် ဘာသာစကားပါ။ သင်ရတာလွယ်ကူပြီး UI တည်ဆောက်တဲ့နေရာမှာ အရမ်းအသုံးဝင်ပါတယ်။
- **IDE (Integrated Development Environment):** Code ရေးတာ၊ ပြင်တာ၊ app ကို run တာတွေလုပ်ဖို့အတွက် သုံးတဲ့ software ပါ။ Visual Studio Code, Android Studio, IntelliJ IDEA တို့ကတော့ လူသုံးအများဆုံး IDE တွေပါ။
- **Emulator နဲ့ Device:** ကိုယ်ရေးထားတဲ့ app ကို စမ်းသပ်ဖို့အတွက် ကွန်ပျူတာထဲမှာ ဖန်တီးထားတဲ့ ဖုန်းအတု (Emulator) ဒါမှမဟုတ် တကယ့်ဖုန်းအစစ် (Device) တွေကို သုံးနိုင်ပါတယ်။

## Flutter SDK ဆိုတာ ဘာလဲ?
Flutter SDK ဆိုတာက Flutter app တွေတည်ဆောက်ဖို့၊ စမ်းသပ်ဖို့၊ debug လုပ်ဖို့အတွက် လိုအပ်တဲ့ tool တွေအကုန်လုံးကို စုစည်းပေးထားတာပါ။ Command line tool တွေသုံးပြီးတော့ project အသစ်ဖန်တီးတာ၊ app ကို run တာ၊ debug လုပ်တာတွေကို လွယ်လွယ်ကူကူ လုပ်နိုင်ပါတယ်။

## Dart Programming Language
Dart ဆိုတာက Google က ဖန်တီးထားတဲ့ open-source programming language တစ်ခုပါ။ သူ့ရဲ့ syntax က JavaScript, Java တို့နဲ့ ဆင်တူတာကြောင့် သင်ရတာလွယ်ကူပါတယ်။ Dart မှာ AOT (Ahead Of Time) နဲ့ JIT (Just In Time) compilation နှစ်မျိုးလုံးပါဝင်တာကြောင့် app ကို run တဲ့အခါမှာ မြန်မြန်ဆန်ဆန်နဲ့ startup လုပ်နိုင်ပါတယ်။

## IDE တွေ
Flutter app တွေကို အဓိကအားဖြင့် IDE သုံးခုနဲ့ ရေးနိုင်ပါတယ်။
- **VS Code:** ပေါ့ပေါ့ပါးပါးနဲ့ သုံးရတာလွယ်ကူပြီး extension တွေလည်း အများကြီးရှိပါတယ်။
- **Android Studio & IntelliJ IDEA:** Flutter အတွက် သီးသန့် tool တွေ၊ feature တွေ ပိုပြီးအစုံအလင်ပါဝင်ပါတယ်။

## Emulator နဲ့ Device
- **Emulator:** ကွန်ပျူတာထဲမှာ ဖုန်းတစ်လုံးလိုမျိုး simulation လုပ်ပေးတဲ့ virtual device ပါ။ App ကို အမြန်စမ်းသပ်ချင်တဲ့အခါမျိုးမှာ အသုံးဝင်ပါတယ်။
- **Device:** ကိုယ်ရေးထားတဲ့ app ကို တကယ့်ဖုန်းအစစ်ပေါ်မှာ run ပြီး စမ်းသပ်တာကတော့ အကောင်းဆုံးပါပဲ။

## App တစ်ခုတည်ဆောက်တဲ့ လုပ်ငန်းစဉ်
၁. Flutter SDK ကိုသုံးပြီး project အသစ်တစ်ခု ဖန်တီးလိုက်ပါ။
၂. Dart language ကိုသုံးပြီး app ရဲ့ logic တွေကို ရေးပါ။ (ဥပမာ - to-do list app)
၃. Stateful widget တွေကိုသုံးပြီး app ရဲ့ state ကို စီမံခန့်ခွဲပါ။
၄. Emulator ဒါမှမဟုတ် တကယ့် device မှာ app ကို run ပြီး စမ်းသပ်ပါ။
၅. IDE မှာပါတဲ့ debugging tool တွေကိုသုံးပြီး bug တွေကို ရှာဖွေပြင်ဆင်ပါ။
၆. အားလုံးအဆင်ပြေပြီဆိုရင်တော့ ကိုယ့် app ကို အသုံးပြုသူတွေဆီ ဖြန့်ချိနိုင်ပါပြီ။

## အနှစ်ချုပ်
Flutter development environment မှာ SDK, Dart, IDE, emulator နဲ့ device တွေပါဝင်ပါတယ်။ ဒီ tool တွေကို ကောင်းကောင်းအသုံးချနိုင်ပြီဆိုရင်တော့ အရည်အသွေးမြင့်တဲ့ cross-platform app တွေကို လွယ်လွယ်ကူကူ တည်ဆောက်နိုင်မှာပါ။