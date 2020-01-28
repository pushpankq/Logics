# Logics

## Break array in chucks 
```swift
let numbers = [2,3,4,5,6,7,8,9,0]

extension Array {
    func chuncked(into size: Int) -> [[Element]] {
        return stride(from: 0, to: count, by: size).map {
            Array(self[$0..<Swift.min($0 + size, count)])
        }
    }
}
```
