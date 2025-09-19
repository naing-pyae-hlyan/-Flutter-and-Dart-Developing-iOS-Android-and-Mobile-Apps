
# Interaction နှင့် Forms များ

Flutter တွင် user interaction များအတွက် widgets များစွာရှိသည်။

## ElevatedButton (Button)
```dart
ElevatedButton(
	onPressed: () { print('Button Pressed'); },
	child: Text('Press Me'),
)
```

## TextField (Text Input)
```dart
TextField(
	decoration: InputDecoration(hintText: 'Enter your name'),
)
```

## Form & Validation
```dart
final _formKey = GlobalKey<FormState>();

Form(
	key: _formKey,
	child: Column(
		children: [
			TextFormField(
				validator: (value) {
					if (value == null || value.isEmpty) {
						return 'အကယ်၍ ဖြည့်ရန်လိုအပ်သည်';
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

## GestureDetector (Gesture Handling)
```dart
GestureDetector(
	onTap: () { print('Tapped!'); },
	child: Container(color: Colors.blue, width: 100, height: 100),
)
```

Form validation ကိုလည်း လွယ်ကူစွာ ပြုလုပ်နိုင်သည်။