
# Navigation (မျက်နှာပြောင်းခြင်း)

Flutter တွင် မျက်နှာပြောင်းခြင်းအတွက် Navigator widget ကို အသုံးပြုသည်။

## Navigator.push (Screen အသစ်သို့ ပြောင်းခြင်း)
```dart
Navigator.push(
	context,
	MaterialPageRoute(builder: (context) => NewScreen()),
);
```

## Navigator.pop (နောက်သို့ ပြန်သွားခြင်း)
```dart
Navigator.pop(context);
```

## Named Routes (Route name ဖြင့် navigation)
```dart
Navigator.pushNamed(context, '/details');
```

## Passing Data Between Screens
```dart
Navigator.push(
	context,
	MaterialPageRoute(
		builder: (context) => DetailScreen(data: 'Data from previous screen'),
	),
);
```

App တစ်ခုလုံးတွင် navigation ကို စနစ်တကျ စီမံနိုင်သည်။