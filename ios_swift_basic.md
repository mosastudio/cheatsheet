* class instances are passed by reference; structs are passed by value. 

* stride

```swift
    // not included
    for i in stride(from: 0, to: 10, by: 2) {
    }

    // possibly included
    for i in stride(from: 0, through: 10, by: 2) {
    }
```

* [Numbers, Data, and Basic Values](https://developer.apple.com/documentation/foundation/numbers_data_and_basic_values)

  * Int

  * Double

* [Strings and Text](https://developer.apple.com/documentation/foundation/strings_and_text)

  * String

```swift
    //  a collection of characters
    let string1 = "Hello"
    var characters = Array(string1)
    characters.remove(at: 0)
    let string2 = String(characters) // "ello"

    let intValue1 = -10
    let string3 = String(intValue1) // "-10"
    let intValue2 = Int(string3) // type: Int?
    
    let string4 = "abc.defg.h"
    let array = string4.split(separator: ".") // type of each element: Substring
    let string5 = array.joined() // "abcdefg"
    let string6 = array.joined(separator: "----") // "abc----defg----h"
```

```swift
    func hasPrefix(_ prefix: String) -> Bool
    func hasSuffix(_ suffix: String) -> Bool

    func removeFirst() -> Character
    func removeLast() -> Character
    
    func lowercased() -> String
    func uppercased() -> String
```

* [Collections](https://developer.apple.com/documentation/foundation/collections)

  * Array

```swift
    let myArr1 = [String]()
    let myArr2: [String] = []
    let myArr3 = Array(repeating: "Hello", count: 5)
    
    for string in myArr3 {
    }
    
    for index in myArr3.indices {
    }
    
    for (index, string) in myArr3.enumerated() {
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

```swift
    func map<T>(_ transform: (Element) throws -> T) rethrows -> [T]
    func flatMap<SegmentOfResult>(_ transform: (Element) throws -> SegmentOfResult) rethrows -> [SegmentOfResult.Element] where SegmentOfResult : Sequence
    func compactMap<ElementOfResult>(_ transform: (Element) throws -> ElementOfResult?) rethrows -> [ElementOfResult]
    
    let array1 = [1, 2, 3, nil, 4]
    let array2 = array1.map { $0 } // array of optional Int, [1, 2, 3, nil, 4]
    let array3 = array1.compactMap { $0 } // array of Int, [1, 2, 3, 4]
    let array4 = [[[1, 2], [3, 4, nil, 5]], [[6, 7]]]
    let array5 = array4.flatMap { $0 } // array of optional Int, [1, 2, 3, 4, nil, 5, 6, 7]
```

```swift
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
    let dict1 = [String: String]()
    let dict2: [String: String] = [:]
    
    for (key, value) in dict1 {
    }
```

  * Set

```swift
    let set1 = Set<String>()
    let set2: Set<String> = []
    
    // the order of elements is not always the same
    let array1 = [1, 2, 3, 4, 3, 2, 1]
    let set3 = Set(array1) // {1, 3, 4, 2}
    let array2 = Array(set3) // [1, 3, 4, 2]
    
    for num in set3 {
        print("\(num)")
    }
```

```swift
    var count: Int { get }
    
    func contains(_ member: Element) -> Bool
    func insert(_ newMember: Element) -> (inserted: Bool, memberAfterInsert: Element)
    func remove(_ member: Element) -> Element?
```
