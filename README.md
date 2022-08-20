# NumberScroller

![image](https://user-images.githubusercontent.com/47273077/185727237-e35a4bb4-9ad8-4773-a2b2-f5a82527325c.png)

## 1. Building a value

<img width="378" src="https://user-images.githubusercontent.com/47273077/185727266-feb451fa-2bc8-44b9-b389-c02d98357eda.gif">

```swift
struct ContentView: View {
  @State private var number = 0.0

  var body: some View {
    Text("\(number, specifier: "%.1f")")
      .focusable()
      .digitalCrownRotation($number)
  }
}
```

