# အခန်း (၁) – Flutter နှင့် Dart ကို မိတ်ဆက်ခြင်း (အပြည့်အစုံ)

ဒီအခန်းမှာ Flutter framework, Dart programming language, Flutter toolchain, widgets, state management, testing, glossary, quiz, troubleshooting, best practices, နောက်ထပ်နမူနာများစွာပါဝင်သည်။ စတင်လေ့လာသူများအတွက် အလွယ်တကူနားလည်နိုင်အောင် မြန်မာလို ရှင်းလင်းပြောပြထားပါတယ်။


---

## ၃။ Flutter နှင့် အခြား Framework များနှိုင်းယှဉ်ခြင်း

- **Flutter**: Dart, single codebase, UI မြန်, hot reload
- **React Native**: JavaScript, cross-platform, native bridge
- **Xamarin**: C#, .NET
- **Native**: Swift (iOS), Kotlin/Java (Android)

**နှိုင်းယှဉ်ရန် အချက်များ**
- Performance
- Development speed
- Code reusability
- UI customization
- Community support

**Flutter vs React Native**
- Flutter သည် UI rendering ကို Skia engine ဖြင့် တိုက်ရိုက်လုပ်သည်။
- React Native သည် JavaScript bridge ကို အသုံးပြုသည်။

**Flutter vs Native**
- Native သည် platform-specific code ဖြစ်သည်။
- Flutter သည် cross-platform ဖြစ်သည်။

---

## ၄။ Flutter Toolchain

Flutter toolchain တွင် –
- **Flutter SDK**
- **Dart SDK**
- **Flutter Engine**
- **DevTools**
- **Flutter Doctor**
- **Hot Reload**

**DevTools နမူနာ**
```sh
flutter pub global activate devtools
flutter pub global run devtools
```

**Flutter Doctor**
```sh
flutter doctor
```

**Hot Reload vs Hot Restart**
- Hot reload သည် code ပြင်ပြီး UI ကို ချက်ချင်းပြသသည်။
- Hot restart သည် app ကို ပြန်လည်စတင်ပေးသည်။

**Troubleshooting**
- Hot reload မလုပ်ပေးလျှင် hot restart လုပ်ပါ

---

## ၅။ Dart Programming Language အခြေခံ

Dart သည် Flutter app များရေးသားရာတွင် အသုံးပြုသော programming language ဖြစ်သည်။

### ၅.၁ Data Types
```dart
int age = 20;
double price = 9.99;
String name = 'Flutter';
bool isActive = true;
List<int> numbers = [1, 2, 3];
Map<String, int> scores = {'Alice': 90, 'Bob': 85};
Set<String> fruits = {'apple', 'banana'};
```

### ၅.၂ Variables & Constants
```dart
var city = 'Yangon'; // type inference
final country = 'Myanmar'; // value set once
const pi = 3.14159; // compile-time constant
```

### ၅.၃ Functions
```dart
String greet(String name) => 'Hello, $name!';
int add(int a, int b) {
  return a + b;
}
```

### ၅.၄ Control Flow
```dart
if (age > 18) {
  print('Adult');
} else {
  print('Minor');
}
for (var fruit in fruits) {
  print(fruit);
}
```

### ၅.၅ Error Handling
```dart
try {
  int result = 10 ~/ 0;
} catch (e) {
  print('Error: $e');
}
```

## ၁။ Flutter ဆိုတာဘာလဲ?
Flutter သည် Google မှ ထုတ်လုပ်သော open-source framework တစ်ခုဖြစ်ပြီး iOS, Android, Web, Desktop အတွက် app များကို တစ်ခုတည်းသော codebase ဖြင့် ဖန်တီးနိုင်သည်။

**Flutter ၏ အားသာချက်များ**
- တစ်ကြိမ်ရေး၊ နေရာတိုင်း run နိုင် (iOS, Android, Web, Desktop)
- Hot reload ဖြင့် အမြန်ပြင်၊ အမြန်ကြည့်
- UI ကို လွယ်ကူစွာ ဖန်တီးနိုင်
- Native performance နီးပါး
- Community support ကြီးမားသည်

**Flutter ကို ဘာကြောင့် သုံးသင့်သလဲ?**
- Developer productivity မြင့်တက်စေသည်
- UI/UX ကို လွယ်ကူစွာ ပြင်ဆင်နိုင်သည်
- Platform-specific code မလိုအပ်ဘူး

**Flutter app များကို ဘယ်လို run လုပ်လဲ?**
- Android, iOS, Web, Desktop တို့တွင် တစ်ပြိုင်နက်တည်း run နိုင်သည်

**Flutter ၏ အဓိက အစိတ်အပိုင်းများ**
- Widgets, Dart, Flutter Engine, DevTools, Hot Reload

---

## ၂။ Flutter Development Environment ကို ပြင်ဆင်ခြင်း

### ၂.၁ လိုအပ်သော Tools များ
- Flutter SDK
- Dart SDK (Flutter SDK ထဲတွင်ပါဝင်သည်)
- IDE (VS Code, Android Studio, IntelliJ)
- Emulator/Device

### ၂.၂ Installation Steps
```sh
flutter doctor
flutter create my_app
cd my_app
flutter run
```
**Tips:**
- `flutter doctor` ဖြင့် setup ပြည့်စုံမှု စစ်ဆေးပါ
- Android/iOS emulator သို့မဟုတ် real device တစ်ခု သုံးပါ

### ၂.၃ Project Structure
```
my_app/
  lib/
    main.dart
    screens/
    widgets/
  assets/
  pubspec.yaml
```
**Best Practice:**
- Code ကို screens, widgets, models အလိုက် ခွဲထားပါ

### ၂.၄ Troubleshooting
- SDK path မမှန်လျှင် `flutter doctor --android-licenses` သုံးပါ
- pubspec.yaml မှာ asset path မှားလျှင် build error ဖြစ်နိုင်သည်

---


**DevTools နမူနာ**
```sh
flutter pub global activate devtools
flutter pub global run devtools
```

---

## ၅။ Dart Programming Language အခြေခံ
Dart သည် Flutter app များရေးသားရာတွင် အသုံးပြုသော programming language ဖြစ်သည်။

**Data Types နမူနာ**
```dart
int age = 20;
double price = 9.99;
String name = 'Flutter';
bool isActive = true;
List<int> numbers = [1, 2, 3];
Map<String, int> scores = {'Alice': 90, 'Bob': 85};
Set<String> fruits = {'apple', 'banana'};
```

**Function နမူနာ**
```dart
String greet(String name) => 'Hello, $name!';
```

---

## ၆။ Flutter Widgets များ
Flutter တွင် UI ကို widget များဖြင့် တည်ဆောက်သည်။
- **StatelessWidget**: ပြောင်းလဲမှုမရှိသော UI
- **StatefulWidget**: ပြောင်းလဲနိုင်သော UI
- **Container, Row, Column**: Layout
- **Text, Image, Icon**: Content
- **Button, TextField**: Interaction

**StatelessWidget နမူနာ**
```dart
class MyText extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text('Hello, Flutter!');
  }
}
```

---

## ၇။ State Management
App ၏ state ကို စီမံရန် –
- **Provider** package
- **setState** method

**StatefulWidget နမူနာ**
```dart
class Counter extends StatefulWidget {
  @override
  _CounterState createState() => _CounterState();
}
class _CounterState extends State<Counter> {
  int count = 0;
  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text('Count: $count'),
        ElevatedButton(
          onPressed: () => setState(() => count++),
          child: Text('Add'),
        ),
      ],
    );
  }
}
```

---

## ၈။ Testing
Flutter app ကို စမ်းသပ်ရန် –
- **flutter_test** package
- **Emulator/Device**

**Unit Test နမူနာ**
```dart
test('adds two numbers', () {
  expect(add(2, 3), 5);
});
```

---

## ၉။ Glossary (အဓိပ္ပါယ်ရှင်းလင်းချက်များ)
| Term | Definition |
|------|------------|
| Code reusability | တစ်ခုတည်းသော codebase ဖြင့် platform များစွာအတွက် app ဖန်တီးနိုင်ခြင်း |
| Dart Analyzer | Dart code error & style စစ်ဆေး tool |
| Flutter DevTools | Debug & performance tools |
| Hot reload | Code ပြင်ပြီး ချက်ချင်း UI တွင် မြင်နိုင်ခြင်း |
| Stateful Widget | ပြောင်းလဲနိုင်သော UI |
| Stateless Widget | ပြောင်းလဲမှုမရှိသော UI |
| ... | ... |

---

## ၁၀။ Quiz (စမ်းသပ်မေးခွန်းများ)
1. Flutter ၏ အားသာချက်တစ်ခုမှာ?
2. Dart Analyzer ၏ အဓိပ္ပါယ်?
3. Flutter SDK ၏ အဓိပ္ပါယ်?
4. StatefulWidget နှင့် StatelessWidget မတူသည့်အချက်?

---

## ၁၁။ အကျဉ်းချုပ်
- Flutter သည် cross-platform app development အတွက် အကောင်းဆုံး framework တစ်ခုဖြစ်သည်။
- Dart သည် UI development အတွက် အထူးသင့်တော်သည်။
- Widgets, state management, testing, DevTools စသည်တို့ကို နားလည်ထားပါ။

---

အခန်း (၁) ကို ပြီးဆုံးပါပြီ။ နောက်ထပ်အခန်းများတွင် ပိုမိုအကြမ်းဖျင်းသော နည်းလမ်းများကို လေ့လာနိုင်ပါသည်။
