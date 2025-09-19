
# Routing (Route စီမံခြင်း)

Flutter တွင် route များကို စီမံရန် named routes နှင့် MaterialPageRoute ကို အသုံးပြုသည်။

## MaterialPageRoute
```dart
Navigator.push(
	context,
	MaterialPageRoute(builder: (context) => SecondScreen()),
);
```

## Named Routes
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

## Route Settings (Parameter Passing)
```dart
Navigator.push(
	context,
	MaterialPageRoute(
		builder: (context) => DetailScreen(data: 'Hello'),
		settings: RouteSettings(arguments: 'Some Data'),
	),
);
```

Route များကို စနစ်တကျ စီမံခြင်းဖြင့် app ၏ structure ကို ပိုမိုကောင်းမွန်စေသည်။