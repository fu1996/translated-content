---
title: Generator.prototype.next()
slug: Web/JavaScript/Reference/Global_Objects/Generator/next
tags:
  - ECMAScript 2015
  - Generator
  - JavaScript
  - Method
  - Prototype
  - Reference
translation_of: Web/JavaScript/Reference/Global_Objects/Generator/next
---
{{JSRef}}

**`next()`** メソッドは、2 つのプロパティ `done` と `value` を持つオブジェクトを返します。 `next` メソッドに引数を提供して、ジェネレーターへ値を送ることもできます。

## 構文

```
gen.next(value)
```

### 引数

<dl><dt><code><var>value</var></code></dt><dd>ジェネレーターへ送る値です。</dd><dd>この値は <code>yield</code> 式の結果として代入されます。例えば <code><var>variable</var> = yield <var>expression</var></code> の場合、 <code>.next()</code> 関数に渡された値は <code><var>variable</var></code> に代入されます。</dd></dl>

### 返値

以下の２つのプロパティを持った {{jsxref("Object")}} です。

<dl><dt><code>done</code> (boolean)</dt><dd>イテレーターが反復処理の末尾を過ぎている場合、値は <code>true</code> になります。この場合、 <code>value</code> はオプションでそのイテレーターの<em>返値</em>を指定します。</dd><dd>イテレーターが反復処理の次の値を生成することができた場合、値は <code>false</code> になります。これは <code>done</code> プロパティを指定しない場合も同等です。</dd><dt><code>value</code></dt><dd>イテレーターが返す何らかの JavaScript の値です。 <code>done</code> が <code>true</code> の場合は省略可能です。</dd></dl>

## 例

### next() の使用

次の例では、 `next` メソッドが返す簡単なジェネレーターとオブジェクトを示します。

```js
function* gen() {
  yield 1;
  yield 2;
  yield 3;
}

const g = gen(); // "Generator { }"
g.next();      // "Object { value: 1, done: false }"
g.next();      // "Object { value: 2, done: false }"
g.next();      // "Object { value: 3, done: false }"
g.next();      // "Object { value: undefined, done: true }"
```

### リストでの next() の使用

```
function* getPage(pageSize = 1, list) {
    let output = [];
    let index = 0;

    while (index < list.length) {
        output = [];
        for (let i = index; i < index + pageSize; i++) {
            if (list[i]) {
                output.push(list[i]);
            }
        }

        yield output;
        index += pageSize;
    }
}

list = [1, 2, 3, 4, 5, 6, 7, 8]
var page = getPage(3, list);              // Generator { }

page.next();                              // Object {value: (3) [1, 2, 3], done: false}
page.next();                              // Object {value: (3) [4, 5, 6], done: false}
page.next();                              // Object {value: (2) [7, 8], done: false}
page.next();                              // Object {value: undefined, done: true}
```

### ジェネレーターへ値を送る

この例では `next` を値付きで呼び出しています。

なお、最初の呼び出しではジェネレーターが何も生成していないため、何もログを記録しないことに注意してください。

```js
function* gen() {
  while (true) {
    let value = yield null;
    console.log(value);
  }
}

const g = gen();
g.next(1);
// "{ value: null, done: false }"
g.next(2);
// 2
// "{ value: null, done: false }"
```

## 仕様書

| 仕様書                                                                                                           |
| ---------------------------------------------------------------------------------------------------------------- |
| {{SpecName('ESDraft', '#sec-generator.prototype.next', 'Generator.prototype.next')}} |

## ブラウザーの互換性

{{Compat("javascript.builtins.Generator.next")}}

## 関連情報

- {{jsxref("Statements/function*", "function*")}}
- [イテレーターとジェネレーター](/ja/docs/Web/JavaScript/Guide/Iterators_and_Generators)
