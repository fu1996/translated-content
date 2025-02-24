---
title: 409 Conflict
slug: Web/HTTP/Status/409
tags:
  - HTTP
  - HTTPステータスコード
  - Reference
  - クライアントエラー
translation_of: Web/HTTP/Status/409
---
{{HTTPSidebar}}

HTTP **`409 Conflict`** はリクエストが現在のサーバーの状態と競合したことを示すステータスコード。

競合は {{HTTPMethod("PUT")}} メソッドを使用したリクエストのレスポンスで最も発生しやすい。例えば、サーバーにすでに存在しているファイルよりも古いバージョンのファイルをアップロードした際に 409 の応答が返され、バージョン管理システムの競合が発生する可能性がある。

## ステータス

```
409 Conflict
```

## 仕様

| 仕様書                                                   | タイトル                                                      |
| -------------------------------------------------------- | ------------------------------------------------------------- |
| {{RFC("7231", "409 Conflict" , "6.5.8")}} | Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content |

## 参照

- {{HTTPMethod("PUT")}}
