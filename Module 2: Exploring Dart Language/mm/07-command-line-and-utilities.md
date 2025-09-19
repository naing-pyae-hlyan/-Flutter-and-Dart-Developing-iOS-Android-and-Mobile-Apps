# Dart Command Line Tools နဲ့ Utilities

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Dart SDK, dart command, pub tool, dart dev tools နဲ့ third-party utilities တွေကို ပေါ့ပေါ့ပါးပါးနဲ့ ရှင်းပြပေးသွားမှာပါ။ Command line tool တွေသုံးတတ်ရင် project တစ်ခုကို အလွယ်တကူ စီမံခန့်ခွဲနိုင်ပါတယ်။

## Dart SDK
- Dart SDK က Dart app တွေဖန်တီးဖို့အတွက် tool, library တွေပါဝင်ပါတယ်။
- dart.dev မှာ OS အလိုက် download လုပ်ပြီး install လုပ်နိုင်ပါတယ်။

## dart Command
- Dart code run, package စီမံ, project ဖန်တီး, code format, test run စတာတွေကို command line မှာလုပ်နိုင်တယ်။

```sh
dart run my_script.dart
# Code ကို run လုပ်တယ်

dart analyze .
# Code error, warning စစ်တယ်

dart test
# Test run လုပ်တယ်

dart format .
# Code ကို format လုပ်တယ်

dart create my_project
# Project အသစ်ဖန်တီးတယ်
```

## Pub Tool
- Dependency စီမံဖို့ package manager ပါ။

```sh
dart pub add http
# http package ကို project ထဲထည့်တယ်

dart pub get
# dependency တွေ install လုပ်တယ်

dart pub upgrade
# dependency တွေ update လုပ်တယ်

dart pub publish
# ကိုယ်ရေးထားတဲ့ package ကို Dart repository ထဲ publish လုပ်တယ်
```

## Dart DevTools
- Performance, debugging, memory analysis, widget inspector စတာတွေကို web interface မှာကြည့်နိုင်တယ်။
- CPU, memory usage, widget tree, bug တွေကို visual နဲ့ စစ်နိုင်တယ်။

## Third-party Tools
- **Shell scripting:** Repetitive task တွေကို automate လုပ်နိုင်တယ်။
- **Makefile:** Project build, test, deploy စတာတွေ rule-based နဲ့ automate လုပ်နိုင်တယ်။
- **CI (Continuous Integration):** GitHub Actions, Travis CI, Circle CI တို့နဲ့ code quality, test, deploy ကို automate လုပ်နိုင်တယ်။

## အနှစ်ချုပ်
- Dart SDK, dart command, pub tool, dev tools, shell script, makefile, CI စတဲ့ tool တွေသုံးတတ်ရင် project တစ်ခုကို အရမ်းလွယ်ကူစွာ စီမံနိုင်ပါတယ်။
- Command line tool တွေသုံးပြီး code quality, test, dependency, deploy စတာတွေကို အချိန်တိုအတွင်း ပြီးမြောက်အောင်လုပ်နိုင်ပါတယ်။
