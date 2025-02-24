---
title: Document.fonts
slug: Web/API/Document/fonts
tags:
  - API
  - DOM
  - Font Loading API
  - FontFace
  - FontFaceSet
  - Fonts
  - フォント
translation_of: Web/API/Document/fonts
---
{{APIRef("DOM")}}

**`fonts`** は {{domxref("Document")}} インターフェイスのプロパティで、文書の {{domxref("FontFaceSet")}} インターフェイスを返します。

## 構文

```
let fontFaceSet = document.fonts;
```

### 値

返値は文書の {{domxref("FontFaceSet")}} インターフェイスです。 `FontFaceSet` インターフェイスは新しいフォントを読み込んだり、以前読み込まれたフォントの状態をチェックしたりするのに有用です。

## 例

### すべてのフォントが読み込まれた後の操作の実行

```js
document.fonts.ready.then(function() {
  // すべてのフォントが読み込まれた後にのみ実行する必要がある操作を
  // ここに記述します。
});
```

## 仕様書

| 仕様書                                                                                           | 状態                                     | 備考     |
| ------------------------------------------------------------------------------------------------ | ---------------------------------------- | -------- |
| {{SpecName('CSS3 Font Loading','#FontFaceSet-interface','FontFaceSet')}} | {{Spec2('CSS3 Font Loading')}} | 初回定義 |

## ブラウザーの互換性

{{Compat}}

## 関連情報

- {{domxref("FontFaceSet")}} インターフェイス
- {{domxref("FontFace")}}
