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

## 2. Limiting the scroll range

<img width="378" src="https://user-images.githubusercontent.com/47273077/185727403-594cf244-41e5-4e2c-b240-2db1d92fde14.gif">

```swift
struct ContentView: View {
  @State private var number = 0.0

  var body: some View {
    Text("\(number, specifier: "%.1f")")
      .focusable()
      .digitalCrownRotation($number, from: 0.0, through: 12.0, by: 0.1)
  }
}
```
