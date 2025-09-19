
# ကျွမ်းကျင်သူအမြင်များ – Flutter Widgets နှင့် Catalog

Flutter တွင် widget catalog သည် UI ဖန်တီးရာတွင် အလွန်အရေးကြီးသည်။

## Basic Widgets
- **Text**
- **Image**
- **Icon**
- **Button**
```dart
Text('Text Widget')
Image.asset('assets/logo.png')
Icon(Icons.home)
ElevatedButton(onPressed: () {}, child: Text('Button'))
```

## Layout Widgets
- **Row**
- **Column**
- **Stack**
- **Container**
```dart
Row(children: [Text('A'), Text('B')])
Column(children: [Text('1'), Text('2')])
Stack(children: [Container(color: Colors.red), Positioned(child: Text('Top'))])
Container(color: Colors.blue, child: Text('Container'))
```

## Input Widgets
- **TextField**
- **Checkbox**
- **Radio**
```dart
TextField()
Checkbox(value: true, onChanged: (v) {})
Radio(value: 1, groupValue: 1, onChanged: (v) {})
```

## Interaction Widgets
- **GestureDetector**
- **InkWell**
```dart
GestureDetector(onTap: () {}, child: Text('Tap Me'))
InkWell(onTap: () {}, child: Icon(Icons.touch_app))
```

Catalog ကို လေ့လာခြင်းဖြင့် UI ကို ပိုမိုမြန်မြန်ဆန်ဆန် ဖန်တီးနိုင်သည်။