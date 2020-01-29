# 文字列変換について
## Int -> String
1. Stringクラスのイニシャライザを使う
2. インスタンスのdescriptionパラメータを使う
3. 文字列補完（文字列展開？）を行う

### 速度比較

```swift
import Foundation
let target: Int = 4792233720368547758

let startA = Date()
let initializer = String(target)
let elapsedA = Date().timeIntervalSince(startA)

let startB = Date()
let description = target.description
let elapsedB = Date().timeIntervalSince(startB)

let startC = Date()
let exp = "\(target)"
let elapsedC = Date().timeIntervalSince(startC)

print(String(format: "%.16f", elapsedA))
print(String(format: "%.16f",elapsedB))
print(String(format: "%.16f", elapsedC))
```

何回かやってだいたい以下の数値
```
0.0000569820404053
0.0001059770584106
0.0000009536743164
```

#### 備考
文字列補完は速度が大きく揺れる条件があった気がする...
