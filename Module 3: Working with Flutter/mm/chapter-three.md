
# အခန်း (၃) – Flutter ဖြင့် အလုပ်လုပ်ခြင်း (အပြည့်အစုံ)

ဒီအခန်းမှာ Flutter app တစ်ခုကို စတင်ဖန်တီးခြင်းမှ စ၍ widgets, forms, navigation, routing, style, UI design, cheat sheet, troubleshooting, best practices, advanced usage, နောက်ထပ်နမူနာများစွာပါဝင်သည်။ စတင်လေ့လာသူများအတွက် အလွယ်တကူနားလည်နိုင်အောင် မြန်မာလို ရှင်းလင်းပြောပြထားပါတယ်။

---

## ၁။ Flutter App Development Process (လုပ်ငန်းစဉ်)

### ၁.၁ Project Setup
Flutter SDK ကို install လုပ်ပြီး project အသစ်တစ်ခု ဖန်တီးပါ။
```sh
flutter create my_app
cd my_app
flutter run
```
**Tips:**
- Project name သည် lowercase, underscore သာပါဝင်ရမည်။
- VS Code သို့မဟုတ် Android Studio ကို အသုံးပြုပါ။

### ၁.၂ Folder Structure
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
- Code ကို screens, widgets, models အလိုက် ခွဲထားပါ။

### ၁.၃ UI Design
Widgets များကို အသုံးပြု၍ UI တည်ဆောက်ပါ။
```dart
Scaffold(
  appBar: AppBar(title: Text('My App')),
  body: Center(child: Text('Hello Flutter!')),
)
```

### ၁.၄ Logic Development
Dart ဖြင့် logic ရေးပါ။
```dart
int add(int a, int b) => a + b;
```

### ၁.၅ State Management
App ၏ state ကို စီမံရန် setState, Provider, Riverpod, Bloc စသည်တို့ကို အသုံးပြုနိုင်သည်။
```dart
setState(() => count++);
```

### ၁.၆ Testing
Emulator/device တွင် စမ်းသပ်ပါ။
```sh
flutter run
```
Unit test, widget test, integration test များရေးနိုင်သည်။

### ၁.၇ Debug & Optimize
DevTools, Flutter Inspector, Hot Reload, Hot Restart ကို အသုံးပြုပါ။
```sh
flutter pub global activate devtools
flutter pub global run devtools
```

### ၁.၈ Deployment
App ကို build & publish လုပ်ပါ။
```sh
flutter build apk # Android
flutter build ios # iOS
```

---

## ၂။ Flutter Widgets များ (အမျိုးအစားအလိုက်)

### ၂.၁ StatelessWidget
ပြောင်းလဲမှုမရှိသော UI
```dart
class MyText extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text('Hello, Flutter!');
  }
}
```

### ၂.၂ StatefulWidget
ပြောင်းလဲနိုင်သော UI
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

### ၂.၃ Layout Widgets
- **Container**
- **Row**
- **Column**
- **Stack**
```dart
Container(
  padding: EdgeInsets.all(8),
  color: Colors.amber,
  child: Text('Container Example'),
)
Row(children: [Text('A'), Text('B')])
Column(children: [Text('One'), Text('Two')])
Stack(children: [Container(color: Colors.red), Positioned(child: Text('Top'))])
```

### ၂.၄ Content Widgets
- **Text**
- **Image**
- **Icon**
```dart
Text('Flutter Ebook')
Image.network('https://flutter.dev/images/flutter-logo-sharing.png')
Icon(Icons.star, color: Colors.yellow)
```

### ၂.၅ Interaction Widgets
- **ElevatedButton**
- **TextField**
```dart
ElevatedButton(onPressed: () {}, child: Text('Click Me'))
TextField(decoration: InputDecoration(hintText: 'Enter text'))
```

### ၂.၆ Advanced Widgets
- **ListView**
- **GridView**
- **Drawer**
- **TabBar**
```dart
ListView.builder(
  itemCount: 10,
  itemBuilder: (context, i) => ListTile(title: Text('Item $i')),
)
GridView.count(
  crossAxisCount: 2,
  children: List.generate(4, (i) => Center(child: Text('Grid $i'))),
)
Drawer(child: ListView(children: [DrawerHeader(child: Text('Header')), ListTile(title: Text('Menu'))]))
TabBar(tabs: [Tab(text: 'A'), Tab(text: 'B')])
```

---

## ၃။ Widget Catalog (ကျွမ်းကျင်သူအမြင်များ)

Flutter ၏ widget catalog တွင် –
- Basic widgets: Text, Image, Icon, Button
- Layout widgets: Row, Column, Stack, Container
- Input widgets: TextField, Checkbox, Radio
- Interaction widgets: GestureDetector, InkWell
- Animation widgets: AnimatedContainer, Hero
- Custom widgets: ကိုယ်တိုင်ဖန်တီးနိုင်သည်

**နမူနာ**
```dart
Checkbox(value: true, onChanged: (v) {})
Radio(value: 1, groupValue: 1, onChanged: (v) {})
GestureDetector(onTap: () {}, child: Text('Tap Me'))
AnimatedContainer(duration: Duration(seconds: 1), color: Colors.red)
```

---

## ၄။ Interaction နှင့် Forms

### ၄.၁ ElevatedButton
```dart
ElevatedButton(
  onPressed: () { print('Button Pressed'); },
  child: Text('Press Me'),
)
```

### ၄.၂ TextField
```dart
TextField(
  decoration: InputDecoration(hintText: 'Enter your name'),
)
```

### ၄.၃ Form & Validation
```dart
final _formKey = GlobalKey<FormState>();
Form(
  key: _formKey,
  child: Column(
    children: [
      TextFormField(
        validator: (value) {
          if (value == null || value.isEmpty) {
            return 'ဖြည့်ရန်လိုအပ်သည်';
          }
          return null;
        },
      ),
      ElevatedButton(
        onPressed: () {
          if (_formKey.currentState!.validate()) {
            // Valid
          }
        },
        child: Text('Submit'),
      ),
    ],
  ),
)
```

### ၄.၄ GestureDetector
```dart
GestureDetector(
  onTap: () { print('Tapped!'); },
  child: Container(color: Colors.blue, width: 100, height: 100),
)
```

### ၄.၅ Advanced Form Example
```dart
class LoginForm extends StatefulWidget {
  @override
  _LoginFormState createState() => _LoginFormState();
}
class _LoginFormState extends State<LoginForm> {
  final _formKey = GlobalKey<FormState>();
  String? email;
  String? password;
  @override
  Widget build(BuildContext context) {
    return Form(
      key: _formKey,
      child: Column(
        children: [
          TextFormField(
            decoration: InputDecoration(labelText: 'Email'),
            validator: (v) => v != null && v.contains('@') ? null : 'Email မှားနေသည်',
            onSaved: (v) => email = v,
          ),
          TextFormField(
            decoration: InputDecoration(labelText: 'Password'),
            obscureText: true,
            validator: (v) => v != null && v.length >= 6 ? null : 'Password အနည်းဆုံး ၆ လုံး',
            onSaved: (v) => password = v,
          ),
          ElevatedButton(
            onPressed: () {
              if (_formKey.currentState!.validate()) {
                _formKey.currentState!.save();
                // Login logic
              }
            },
            child: Text('Login'),
          ),
        ],
      ),
    );
  }
}
```

---

## ၅။ Navigation (မျက်နှာပြောင်းခြင်း)

### ၅.၁ Navigator.push
```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => NewScreen()),
);
```

### ၅.၂ Navigator.pop
```dart
Navigator.pop(context);
```

### ၅.၃ Named Routes
```dart
Navigator.pushNamed(context, '/details');
```

### ၅.၄ Passing Data
```dart
Navigator.push(
  context,
  MaterialPageRoute(
    builder: (context) => DetailScreen(data: 'Data from previous screen'),
  ),
);
```

### ၅.၅ Drawer Navigation
```dart
Drawer(
  child: ListView(
    children: [
      DrawerHeader(child: Text('Header')),
      ListTile(title: Text('Home'), onTap: () {}),
    ],
  ),
)
```

---

## ၆။ Routing

### ၆.၁ MaterialPageRoute
```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondScreen()),
);
```

### ၆.၂ Named Routes
```dart
MaterialApp(
  initialRoute: '/',
  routes: {
    '/': (context) => HomeScreen(),
    '/details': (context) => DetailsScreen(),
  },
)
Navigator.pushNamed(context, '/details');
```

### ၆.၃ Route Settings (Parameter Passing)
```dart
Navigator.push(
  context,
  MaterialPageRoute(
    builder: (context) => DetailScreen(data: 'Hello'),
    settings: RouteSettings(arguments: 'Some Data'),
  ),
);
```

---

## ၇။ Style များ အသုံးပြုခြင်း

### ၇.၁ TextStyle
```dart
Text('Flutter Ebook', style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold, color: Colors.blue, letterSpacing: 2.0, decoration: TextDecoration.underline))
```

### ၇.၂ ButtonStyle
```dart
ElevatedButton(
  style: ElevatedButton.styleFrom(primary: Colors.green, shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(12)), padding: EdgeInsets.symmetric(horizontal: 32, vertical: 16)),
  onPressed: () {},
  child: Text('Submit'),
)
```

### ၇.၃ ThemeData
```dart
MaterialApp(
  theme: ThemeData(
    primarySwatch: Colors.purple,
    brightness: Brightness.light,
    textTheme: TextTheme(bodyText2: TextStyle(fontSize: 18, color: Colors.black87)),
    buttonTheme: ButtonThemeData(buttonColor: Colors.purple, shape: StadiumBorder()),
  ),
  home: MyHomePage(),
)
```

### ၇.၄ Custom Styles
```dart
Container(
  decoration: BoxDecoration(
    color: Colors.orange[100],
    border: Border.all(color: Colors.orange, width: 2),
    borderRadius: BorderRadius.circular(8),
    boxShadow: [BoxShadow(color: Colors.orange.withOpacity(0.3), blurRadius: 8, offset: Offset(2, 4))],
  ),
  child: Padding(padding: EdgeInsets.all(16), child: Text('Custom Styled Box')),
)
```

### ၇.၅ AppBar & ListTile Styling
```dart
AppBar(title: Text('My App'), backgroundColor: Colors.teal, elevation: 4, actions: [IconButton(icon: Icon(Icons.settings), onPressed: () {})])
ListTile(leading: Icon(Icons.person, color: Colors.deepPurple), title: Text('User Name', style: TextStyle(fontWeight: FontWeight.bold)), subtitle: Text('Subtitle text'), trailing: Icon(Icons.arrow_forward_ios), tileColor: Colors.grey[200])
```

---

## ၈။ UI Design (ကျွမ်းကျင်သူအမြင်များ)

### ၈.၁ Consistency
Theme, layout, color, font တူညီမှု
```dart
ThemeData(primarySwatch: Colors.blue)
```

### ၈.၂ Responsiveness
Screen အရွယ်အစားအလိုက် ပြောင်းလဲနိုင်သော UI
```dart
LayoutBuilder(
  builder: (context, constraints) {
    if (constraints.maxWidth > 600) {
      return WideLayout();
    } else {
      return NarrowLayout();
    }
  },
)
```

### ၈.၃ Accessibility
Semantics, contrast, font size
```dart
Semantics(label: 'Submit Button', child: ElevatedButton(onPressed: () {}, child: Text('Submit')))
```

### ၈.၄ Performance
Efficient widgets, lazy loading
```dart
ListView.builder(itemCount: 1000, itemBuilder: (context, index) => Text('Item $index'))
```

### ၈.၅ UX Tips
- Loading indicator, error message, empty state
```dart
if (isLoading) return CircularProgressIndicator();
if (hasError) return Text('Error!');
if (items.isEmpty) return Text('No data');
```

---

## ၉။ Troubleshooting & Common Mistakes

- Widget tree မမှန်ခြင်း (UI မထွက်ခြင်း)
- setState ကို StatelessWidget မှာ သုံးခြင်း
- context မမှန်သောနေရာတွင် Navigator သုံးခြင်း
- pubspec.yaml မှာ asset path မှားခြင်း
- Hot reload မလုပ်ပေးခြင်း (Hot restart လုပ်ပါ)

**Troubleshooting Example**
```dart
// setState ကို StatelessWidget မှာ သုံးလို့မရပါ
// StatelessWidget မှာ state မရှိပါ
```

---

## ၁၀။ Cheat Sheet

- **ElevatedButton**
```dart
ElevatedButton(onPressed: () {}, child: Text('Press'))
```
- **TextField**
```dart
TextField(decoration: InputDecoration(hintText: 'Enter text'))
```
- **Navigator.push**
```dart
Navigator.push(context, MaterialPageRoute(builder: (_) => NewScreen()))
```
- **TextStyle**
```dart
Text('Styled', style: TextStyle(fontWeight: FontWeight.bold))
```
- **DropdownButton**
```dart
DropdownButton<String>(
  value: 'One',
  items: ['One', 'Two'].map((v) => DropdownMenuItem(value: v, child: Text(v))).toList(),
  onChanged: (v) {},
)
```
- **ListView**
```dart
ListView(children: [Text('A'), Text('B')])
```
- **Dialog**
```dart
showDialog(context: context, builder: (_) => AlertDialog(title: Text('Alert')))
```
- **CustomPaint**
```dart
CustomPaint(painter: MyPainter())
```
- **ExpansionPanel**
```dart
ExpansionPanelList(expansionCallback: (i, isOpen) {}, children: [],)
```

---

## ၁၁။ Exercises & Quiz

### ၁၁.၁ Practice
1. StatelessWidget, StatefulWidget ကို သီးသန့်ရေးပါ။
2. ListView, GridView ကို အသုံးပြု၍ UI တစ်ခုရေးပါ။
3. Form validation logic ကို ကိုယ်တိုင်ရေးပါ။
4. Navigator.push, pop, named routes ကို အသုံးပြုပါ။
5. ThemeData, custom style ကို သုံးပြီး UI တစ်ခုရေးပါ။

### ၁၁.၂ Quiz
1. Flutter app တစ်ခုဖန်တီးရာတွင် အရေးကြီးဆုံး widgets သုံးခုရေးပါ။
2. StatefulWidget နှင့် StatelessWidget မတူသည့်အချက်?
3. Navigator.push နှင့် Navigator.pushNamed မတူသည့်အချက်?
4. Form validation ကို ဘယ်လိုလုပ်သလဲ?
5. ThemeData သည် ဘာအတွက်သုံးသလဲ?

---

## ၁၂။ အကျဉ်းချုပ်
- Flutter app တစ်ခုကို စတင်ဖန်တီးခြင်းမှ စ၍ advanced UI, navigation, style, cheat sheet, troubleshooting, best practices အထိ လေ့လာနိုင်ပါသည်။
- နမူနာ code များ၊ exercises, quiz များပါဝင်သဖြင့် စတင်လေ့လာသူများအတွက် အလွယ်တကူနားလည်နိုင်ပါသည်။
- Flutter documentation ကို အမြဲလေ့လာပါ။

---

အခန်း (၃) ကို ပြီးဆုံးပါပြီ။ Flutter app တစ်ခုကို စတင်ဖန်တီးခြင်းမှ စ၍ advanced UI, navigation, style, cheat sheet, troubleshooting, best practices အထိ လေ့လာနိုင်ပါသည်။
