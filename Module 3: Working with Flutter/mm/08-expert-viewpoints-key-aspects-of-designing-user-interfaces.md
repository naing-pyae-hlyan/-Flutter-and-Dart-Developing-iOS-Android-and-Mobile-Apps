
# ကျွမ်းကျင်သူအမြင်များ – UI Design

Flutter တွင် UI ကို ဖန်တီးရာတွင် အရေးကြီးသော အချက်များမှာ –

## Consistency (တူညီမှု)
- Layout နှင့် style တူညီမှု
```dart
ThemeData(primarySwatch: Colors.blue)
```

## Responsiveness (Device များအလိုက် ပြောင်းလဲနိုင်မှု)
- Screen အရွယ်အစားအလိုက် ပြောင်းလဲနိုင်သော UI
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

## Accessibility (အသုံးဝင်မှု)
- Semantics, contrast, font size
```dart
Semantics(
	label: 'Submit Button',
	child: ElevatedButton(onPressed: () {}, child: Text('Submit')),
)
```

## Performance (မြန်မြန်ဆန်ဆန် run နိုင်မှု)
- Efficient widgets, lazy loading
```dart
ListView.builder(
	itemCount: 1000,
	itemBuilder: (context, index) => Text('Item $index'),
)
```

UI design ကို ဦးစားပေးခြင်းသည် app ၏ အောင်မြင်မှုအတွက် အရေးကြီးသည်။