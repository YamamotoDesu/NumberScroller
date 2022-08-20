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


---------
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


---------
## 3. Sensitivity

### ■ .heigh
```swift
    Text("\(number, specifier: "%.1f")")
      .focusable()
      .digitalCrownRotation(
        $number,
        from: 0.0,
        through: 12.0,
        by: 0.1,
        sensitivity: .high
      )
 ```
 
 <img width="378" src="https://user-images.githubusercontent.com/47273077/185727543-c9481cdc-48bb-48c5-9292-d006c52cf4d6.gif">
 
 ### ■ .midium 
 ```swift
     Text("\(number, specifier: "%.1f")")
      .focusable()
      .digitalCrownRotation(
        $number,
        from: 0.0,
        through: 12.0,
        by: 0.1,
        sensitivity: .medium
      )
  ```

<img width="378" src="https://user-images.githubusercontent.com/47273077/185727596-8f496d53-cb6c-4624-97f3-4f09f606528b.gif">


 ### ■ .low 
 ```swift
     Text("\(number, specifier: "%.1f")")
      .focusable()
      .digitalCrownRotation(
        $number,
        from: 0.0,
        through: 12.0,
        by: 0.1,
        sensitivity: .low
      )
  ```

<img width="378" src="https://user-images.githubusercontent.com/47273077/185727654-53b22d9e-0b39-44e3-8db8-fa0e593899b0.gif">

---------
## 4. Wrapping around
```swift
    Text("\(number, specifier: "%.1f")")
      .focusable()
      .digitalCrownRotation(
        $number,
        from: 0.0,
        through: 12.0,
        by: 0.1,
        sensitivity: .low,
        isContinuous: true
      )
```

<img width="378" src="https://user-images.githubusercontent.com/47273077/185730588-38de92d3-68a4-49e8-9ca3-4d2c5f6dc775.gif">





