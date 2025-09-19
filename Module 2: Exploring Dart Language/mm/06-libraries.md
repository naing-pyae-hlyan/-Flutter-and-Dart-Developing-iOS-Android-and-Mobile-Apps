# Dart မှာ Library များ အသုံးပြုနည်း

မိတ်ဆွေတို့ရေ၊ ဒီအခန်းမှာတော့ Dart ဘာသာစကားမှာ အသုံးများတဲ့ library များ၊ import နည်း၊ ကိုယ်ပိုင် library ဖန်တီးနည်းတွေကို ပေါ့ပေါ့ပါးပါးနဲ့ ရှင်းပြပေးသွားမှာပါ။

## Dart Core Library
- Dart core library က basic data type, collection, utility function တွေပါဝင်ပါတယ်။
- ဒီ library ကို import မလုပ်ဘဲ default ပါဝင်ပါတယ်။

```dart
var greeting = 'Hello';
int age = 20;
var fruits = ['apple', 'banana'];
var scores = {'Aung': 90, 'Mya': 85};
```

## dart:math Library
- Math function, constant, random number တွေတွက်အသုံးဝင်တယ်။

```dart
import 'dart:math';
var angle = pi / 4;
print(sin(angle));
var rand = Random();
print(rand.nextInt(100)); // 0-99
```

## dart:async Library
- Async programming (Future, Stream) တွေကို handle လုပ်နိုင်တယ်။

```dart
import 'dart:async';
Future<String> fetchData() async {          
  await Future.delayed(Duration(seconds: 2));
  return 'Data loaded';
}
```

## dart:convert Library
- JSON, UTF-8 encode/decode လုပ်ဖို့ အသုံးဝင်တယ်။

```dart
import 'dart:convert';
var jsonStr = '{"name": "Aung", "age": 20}';
var user = jsonDecode(jsonStr);
var newJson = jsonEncode({'name': 'Mya', 'age': 22});
```

## HTTP Package
- REST API နဲ့ data လှုပ်ရှားဖို့ အသုံးဝင်တယ်။

```dart
import 'package:http/http.dart' as http;
var url = Uri.parse('https://example.com');
var response = await http.get(url);
if (response.statusCode == 200) {
  print(response.body);
}
```

## intl Package
- Localization, date/time format ပြောင်းဖို့ အသုံးဝင်တယ်။

```dart
import 'package:intl/intl.dart';
var now = DateTime.now();
var formatter = DateFormat('yyyy-MM-dd');
print(formatter.format(now));
```

## path Package
- File, directory path တွေကို join, split, normalize လုပ်ဖို့ အသုံးဝင်တယ်။

```dart
import 'package:path/path.dart' as p;
var filePath = p.join('folder', 'file.txt');
```

## ကိုယ်ပိုင် Library ဖန်တီးနည်း
- ကိုယ်ပိုင် reusable code တွေကို library အနေနဲ့ ဖန်တီးနိုင်တယ်။

```dart
// math_utils.dart
library math_utils;
double square(double x) => x * x;

// main.dart
import 'math_utils.dart';
print(square(4)); // Output: 16
```

## အနှစ်ချုပ်
- Dart core, math, async, convert, HTTP, intl, path စတဲ့ library/package တွေက app တည်ဆောက်ရာမှာ အရမ်းအသုံးဝင်တယ်။
- ကိုယ်ပိုင် library ဖန်တီးပြီး import လုပ်သုံးနိုင်တယ်။
- Library တွေသုံးတာနဲ့ code ကို modular, reusable ဖြစ်အောင် စီမံနိုင်ပါတယ်။
