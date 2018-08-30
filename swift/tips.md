## trim
```swift
var str = "AB CD EF"
str = str.trimmingCharacters(in: .whitespaces)
```

## remove all spaces
```swift
var str = "ab cd ed"
str = str.replacingOccurrences(of: " ", with: "")
```

## capitalize and reverse
```swift
var str = "ABC"
str = str.lowercased()
str = str.uppercased()
```