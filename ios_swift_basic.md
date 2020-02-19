* class instances are passed by reference; structs are passed by value. 

* [Numbers, Data, and Basic Values](https://developer.apple.com/documentation/foundation/numbers_data_and_basic_values)

  * Int

  * Double

* [Strings and Text](https://developer.apple.com/documentation/foundation/strings_and_text)

  * String

```
    func hasPrefix(_ prefix: String) -> Bool
    func hasSuffix(_ suffix: String) -> Bool

    func removeFirst() -> Character
    func removeLast() -> Character
```

* [Collections](https://developer.apple.com/documentation/foundation/collections)

  * Array

```swift
    var myArr1 = [String]()
    var myArr2: [String] = []
    
    for string in myArr1 {
    }
    
    for index in myArr1.indices {
    }
    
    for (index, string) in myArr1.enumerated() {
    }
```

```swift
    var count: Int
    var first: Element? { get }
    var last: Element? { get }

    func append(_ newElement: Element)
    func insert(_ newElement: Element, at i: Int)
    func remove(at index: Int) -> Element
    func removeFirst() -> Element
    func removeLast() -> Element
```

```
    func reduce<Result>(_ initialResult: Result, _ nextPartialResult: (Result, Element) throws -> Result) rethrows -> Result
    func min() -> Element?
    func min(by areInIncreasingOrder: (Element, Element) throws -> Bool) rethrows -> Element?
    
    let array = [1, 2, 3, 4, 5]

    let sum1 = array.reduce(0) { (x, y) -> Int in
        return x + y
    } // 15
    let sum2 = array.reduce(0) { (x, y) -> Int in
        x + y
    } // 15
    let sum3 = array.reduce(0) { $0 + $1 } // 15
    let sum4 = array.reduce(0, +) // 15
    let incorrectSum = array.reduce(1, +) // 16, initialResult = 1

    let minimum1 = array.reduce(Int.max) { min($0, $1) } // the type: Int
    let minimum2 = array.min() // the type: Int?
    let minimum3 = array.min { (x, y) -> Bool in
        x < y
    } // the type: Int?
    let minimum4 = array.min { $0 < $1 } // the type: Int?
```

  * Dictionary

```swift
    var dict1 = [String: String]()
    var dict2: [String: String] = [:]
    
    for (key value) in dict1 {
    }
```

  * Set

```swift
    var set1 = Set<String>()
    var set2: Set<String> = []
```
