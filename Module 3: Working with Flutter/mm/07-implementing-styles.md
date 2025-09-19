
# Style များ အသုံးပြုခြင်း (Flutter UI Styling)

Flutter တွင် UI ကို အလှဆင်ရန် style များကို အသုံးပြုနိုင်သည်။

## TextStyle ကို အသုံးပြုပြီး စာသားများကို အလှဆင်ခြင်း
```dart
Text(
	'Flutter Ebook',
	style: TextStyle(
		fontSize: 24,
		fontWeight: FontWeight.bold,
		color: Colors.blue,
		letterSpacing: 2.0,
		decoration: TextDecoration.underline,
	),
)
```

## ButtonStyle ကို အသုံးပြုပြီး Button များကို အလှဆင်ခြင်း
```dart
ElevatedButton(
	style: ElevatedButton.styleFrom(
		primary: Colors.green,
		shape: RoundedRectangleBorder(
			borderRadius: BorderRadius.circular(12),
		),
		padding: EdgeInsets.symmetric(horizontal: 32, vertical: 16),
	),
	onPressed: () {},
	child: Text('Submit'),
)
```

## ThemeData ဖြင့် App တစ်ခုလုံးအတွက် Theme သတ်မှတ်ခြင်း
```dart
MaterialApp(
	theme: ThemeData(
		primarySwatch: Colors.purple,
		brightness: Brightness.light,
		textTheme: TextTheme(
			bodyText2: TextStyle(fontSize: 18, color: Colors.black87),
		),
		buttonTheme: ButtonThemeData(
			buttonColor: Colors.purple,
			shape: StadiumBorder(),
		),
	),
	home: MyHomePage(),
)
```

## Custom Styles (ကိုယ်ပိုင် Style များ)
```dart
Container(
	decoration: BoxDecoration(
		color: Colors.orange[100],
		border: Border.all(color: Colors.orange, width: 2),
		borderRadius: BorderRadius.circular(8),
		boxShadow: [
			BoxShadow(
				color: Colors.orange.withOpacity(0.3),
				blurRadius: 8,
				offset: Offset(2, 4),
			),
		],
	),
	child: Padding(
		padding: EdgeInsets.all(16),
		child: Text('Custom Styled Box'),
	),
)
```

## AppBar ကို အလှဆင်ခြင်း
```dart
AppBar(
	title: Text('My App'),
	backgroundColor: Colors.teal,
	elevation: 4,
	actions: [
		IconButton(icon: Icon(Icons.settings), onPressed: () {}),
	],
)
```

## ListTile ကို အလှဆင်ခြင်း
```dart
ListTile(
	leading: Icon(Icons.person, color: Colors.deepPurple),
	title: Text('User Name', style: TextStyle(fontWeight: FontWeight.bold)),
	subtitle: Text('Subtitle text'),
	trailing: Icon(Icons.arrow_forward_ios),
	tileColor: Colors.grey[200],
)
```

Style များကို သုံးခြင်းဖြင့် app ၏ look & feel ကို တိုးတက်စေသည်။