
# Flutter Widgets များ

Flutter တွင် UI ကို တည်ဆောက်ရာတွင် widget များကို အခြေခံအဖြစ် အသုံးပြုသည်။

## StatelessWidget (ပြောင်းလဲမှုမရှိသော UI)
```dart
class MyText extends StatelessWidget {
	@override
	Widget build(BuildContext context) {
		return Text('Hello, Flutter!');
	}
}
```

## StatefulWidget (ပြောင်းလဲနိုင်သော UI)
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

## Layout Widgets
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

Row(
	children: [Text('A'), Text('B')],
)

Column(
	children: [Text('One'), Text('Two')],
)
```

## Content Widgets
- **Text**
- **Image**
- **Icon**
```dart
Text('Flutter Ebook')
Image.network('https://flutter.dev/images/flutter-logo-sharing.png')
Icon(Icons.star, color: Colors.yellow)
```

## Interaction Widgets
- **ElevatedButton**
- **TextField**
```dart
ElevatedButton(
	onPressed: () {},
	child: Text('Click Me'),
)

TextField(
	decoration: InputDecoration(hintText: 'Enter text'),
)
```

Widget များကို ပေါင်းစပ်၍ UI ကို လွယ်ကူစွာ ဖန်တီးနိုင်သည်။