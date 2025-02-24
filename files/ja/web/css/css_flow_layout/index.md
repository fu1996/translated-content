---
title: CSS フローレイアウト
slug: Web/CSS/CSS_Flow_Layout
tags:
  - CSS
  - Reference
  - ガイド
  - フロー
  - フローレイアウト
  - レイアウト
  - 中級者
translation_of: Web/CSS/CSS_Flow_Layout
---
{{CSSRef}}

_通常フロー_ (Normal Flow) 、またはフローレイアウトは、レイアウトに変更が加えられる前にブロック要素やインライン要素がページに表示される方法です。このフローは本質的に、共に動作するすべてのものの組み合わせで、レイアウトの中で互いについてを知っています。いったん何かが*フローの外*に出ると、独立して動作します。

通常フローでは、**インライン**要素はインライン方向、つまり文書の書字方向に従って、文の中で言葉が表示される方向に表示されます。**ブロック**要素は、文書の[書字方向](/ja/docs/Web/CSS/CSS_Writing_Modes)の中で、段落として一つが他の物の後に表示されます。従って英語では、インライン要素は左から始まり、一つが他の物の後に表示され、ブロック要素は上から始まり、ページの下に向かいます。

## 基本的な例

以下の例はブロック及びインラインレベルボックスの例を示します。緑色の枠線がある二つの要素がブロックレベルで、他の物の下に表示されます。

最初の文は青い背景をもつ span 要素を含んでいます。これはインラインレベルで、文の中に表示されます。

{{EmbedGHLiveSample("css-examples/layout/normal-flow.html", '100%', 720)}}

## ガイド

- [通常フローでのブロック及びインラインレイアウト](/ja/docs/Web/CSS/CSS_Flow_Layout/Block_and_Inline_Layout_in_Normal_Flow)
- [フロー内とフローの外](/ja/docs/Web/CSS/CSS_Flow_Layout/In_Flow_and_Out_of_Flow)
- [Formatting Contexts Explained](/ja/docs/Web/CSS/CSS_Flow_Layout/Formatting_Contexts_Explained)
- [フローレイアウトと書字方向](/ja/docs/Web/CSS/CSS_Flow_Layout/Flow_Layout_and_Writing_Modes)
- [フローレイアウトとオーバーフロー](/ja/docs/Web/CSS/CSS_Flow_Layout/Flow_Layout_and_Overflow)

## リファレンス

### 用語集の記事

- {{Glossary("Block/CSS", "ブロック (CSS)")}}

1.  [**CSS**](/ja/docs/Web/CSS)
2.  [**CSS リファレンス**](/ja/docs/Web/CSS/Reference)
