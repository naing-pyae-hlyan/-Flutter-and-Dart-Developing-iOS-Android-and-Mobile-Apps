
# Cheat Sheet: Flutter ကို လွယ်ကူစွာ အသုံးပြုရန်

## Interaction နှင့် Forms
- **ElevatedButton**
```dart
ElevatedButton(onPressed: () {}, child: Text('Press'))
```
- **TextField**
```dart
TextField(decoration: InputDecoration(hintText: 'Enter text'))
```
- **Form & Validation**
```dart
Form(
	child: TextFormField(
		validator: (v) => v == null || v.isEmpty ? 'Required' : null,
	),
)
```
- **GestureDetector**
```dart
GestureDetector(onTap: () {}, child: Text('Tap'))
```

## Navigation & Routing
- **Navigator.push**
```dart
Navigator.push(context, MaterialPageRoute(builder: (_) => NewScreen()))
```
- **Navigator.pushNamed**
```dart
Navigator.pushNamed(context, '/details')
```
- **Passing data**
```dart
Navigator.push(context, MaterialPageRoute(builder: (_) => DetailScreen(data: 'data')))
```

## Style & UI
- **TextStyle, ButtonStyle, ThemeData**
```dart
Text('Styled', style: TextStyle(fontWeight: FontWeight.bold))
ElevatedButton(style: ElevatedButton.styleFrom(primary: Colors.red), onPressed: () {}, child: Text('Red'))
MaterialApp(theme: ThemeData(primarySwatch: Colors.green))
```
- **Custom styles**
```dart
Container(
	decoration: BoxDecoration(border: Border.all(color: Colors.blue)),
	child: Text('Box'),
)
```

## Widgets
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
- **GridView**
```dart
GridView.count(crossAxisCount: 2, children: [Text('1'), Text('2')])
```
- **SnackBar**
```dart
ScaffoldMessenger.of(context).showSnackBar(SnackBar(content: Text('Message')))
```
- **Dialog**
```dart
showDialog(context: context, builder: (_) => AlertDialog(title: Text('Alert')))
```
- **Padding**
```dart
Padding(padding: EdgeInsets.all(8), child: Text('Pad'))
```
- **ExpansionPanel**
```dart
ExpansionPanelList(
	expansionCallback: (i, isOpen) {},
	children: [],
)
```
- **CustomPaint**
```dart
CustomPaint(painter: MyPainter())
```

နမူနာ code များကို Flutter documentation တွင် ရှာဖွေကြည့်ပါ။