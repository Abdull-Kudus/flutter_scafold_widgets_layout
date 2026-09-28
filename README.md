# Flutter Widget Demo: Scaffold

A simple demonstration of Flutter's `Scaffold` widget for a standard mobile screen.

---

## 1. Use Case

Every mobile screen needs a standard layout structure: a bar at the top, content in the middle, and an action button at the bottom. The `Scaffold` widget provides this exact visual skeleton out of the box so you do not have to position these elements manually.

---

## 2. Code

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MaterialApp(
    home: SimpleScreen(),
  ));
}

class SimpleScreen extends StatelessWidget {
  const SimpleScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('My App'),
        backgroundColor: Colors.blue,
      ),
      body: const Center(
        child: Text(
          'Hello, World!',
          style: TextStyle(fontSize: 24),
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {},
        child: const Icon(Icons.add),
      ),
    );
  }
}

```

---

## 3. Code Explanation (As Me)

First, I wrote the `main()` function to run the application wrapped in a `MaterialApp`.

Next, I created `SimpleScreen` as a `StatelessWidget` because the screen displays static content without changing any state.

Inside the `build` method, I returned the `Scaffold` widget to set up the basic layout frame of the screen.

I assigned an `AppBar` widget to the `appBar` property so that the app displays a blue navigation header with the title "My App".

I passed a centered `Text` widget to the `body` property so the text "Hello, World!" sits directly in the center of the screen.

Finally, I set the `floatingActionButton` property with a simple `FloatingActionButton` holding an add icon at the bottom corner.

---

## 4. The 3 Key Attributes

The `appBar` attribute places a fixed header toolbar at the top of the device screen.

The `body` attribute defines the primary display area where the main content or layout sits.

The `floatingActionButton` attribute adds a circular action button that floats near the bottom-right corner of the screen.

---

## 5. Presentation Script (3–5 Minutes)

"Hello everyone. Today, I am presenting the `Scaffold` widget in Flutter.

The use case here is very straightforward: whenever you build any basic screen in a mobile app, you need a header, a main content area, and an action button. Without `Scaffold`, elements would overlap each other or get cut off by the phone's status bar. `Scaffold` provides that standard framework automatically.

In my code, I created a single screen called `SimpleScreen`. Inside its `build` method, I returned a `Scaffold` widget and configured its three most essential attributes.

First is `appBar`. By passing an `AppBar` widget here, Flutter automatically reserves space at the top of the phone and renders our title, 'My App', with a clean blue background.

Second is `body`. This is where your main screen content lives. I placed a simple centered text widget saying 'Hello, World!' right in the middle of the screen.

Third is `floatingActionButton`. This attribute gives us an elevated circular button in the bottom corner, which is standard for primary actions like creating or adding new items.

In short, `Scaffold` is the foundational building block for creating clean, standard screens in Flutter without manually styling positions.