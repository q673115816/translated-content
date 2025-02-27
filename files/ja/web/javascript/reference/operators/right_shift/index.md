---
title: 右シフト (>>)
slug: Web/JavaScript/Reference/Operators/Right_shift
tags:
  - ビット演算子
  - JavaScript
  - 言語機能
  - 演算子
  - Reference
browser-compat: javascript.operators.right_shift
translation_of: Web/JavaScript/Reference/Operators/Right_shift
---
{{jsSidebar("Operators")}}

**右シフト演算子 (`>>`)** は、1つ目のオペランドを指定されたビット数だけ右にずらします。右にずらしてあふれたビットは廃棄されます。最も左のビットをコピーしながらずれて入ります。最も左のビットが以前の最も左のビットと同じになるため、符号ビット (最も左のビット) は変化しません。よって「符号維持」という名前です。

{{EmbedInteractiveExample("pages/js/expressions-right-shift.html")}}

## 構文

```js
a >> b
```

## 解説

この演算子は、1 つ目のオペランドを指定されたビット数だけ右にずらします。右にずらしてあふれたビットは廃棄されます。最も左のビットをコピーしながらずれて入ります。最も左のビットが以前の最も左のビットと同じになるため、符号ビット (最も左のビット) は変化しません。よって「符号維持」という名前です。

例えば、 `9 >> 2` は 2 となります。

```js
.    9 (10 進数): 00000000000000000000000000001001 (2 進数)
                  --------------------------------
9 >> 2 (10 進数): 00000000000000000000000000000010 (2 進数) = 2 (10 進数)
```

同様に、 `-9 >> 2` は符号が保存されるため、 `-3` になります。

```js
.    -9 (10 進数): 11111111111111111111111111110111 (2 進数)
                   --------------------------------
-9 >> 2 (10 進数): 11111111111111111111111111111101 (2 進数) = -3 (10 進数)
```

## 例

### 右シフトの使用

```js
 9 >> 2; //  2
-9 >> 2; // -3
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- [ビット演算子 (JavaScript ガイド)](/ja/docs/Web/JavaScript/Guide/Expressions_and_Operators#bitwise)
- [右シフト代入演算子](/ja/docs/Web/JavaScript/Reference/Operators/Right_shift_assignment)
