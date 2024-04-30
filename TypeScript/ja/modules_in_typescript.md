---
title: "TypeScriptにおけるモジュール"
description: "GitHub Copilotを使用したTypeScriptのモジュール"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## TypeScriptにおけるモジュール
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
ES6がモジュールの概念を導入したことで、JavaScriptはJavaScriptライブラリの一部としてモジュールの概念をサポートするようになりました。TypeScriptが登場したときも、JavaScriptと同じくモジュールを共有しています。TypeScriptのモジュールは、宣言とそのコードの両方を含むことができます。モジュールはローカル環境で実行され、グローバルスコープでは実行されません。つまり、モジュール内で関数、変数、クラス、インターフェースなどを定義した場合、export文を使用してモジュールをエクスポートしない限り、モジュールの外部からは見えません。モジュール内の変数や関数にアクセスするには、import文を使用してモジュールをファイルにインポートする必要があります。
GitHub Copilotは、TypeScriptでモジュールを作成する方法を案内することができます。ファイルを作成するわけではありませんが、どこにファイルを作成し、ファイルの内容を提案することができます。モジュールをインポートする方法はさまざまです。`tab`キーを押すと、GitHub Copilotはモジュールのインポート方法をすべて提案し、その方法を説明します。例は同じ関数名のためにエラーが発生する場合や、インポートしているファイルが現在存在しない場合がありますが、GitHub Copilotはコードを書く場所を提案するので、それらのファイルを作成してからコンテンツを追加する必要があります。

### 例

##### 入力コード
```TypeScript
// typescript でモジュールを作成するにはどうすればよいですか?
```

##### 副操縦士によって提案された結果
```TypeScript
// typescript でモジュールを作成するにはどうすればよいですか?
// TypeScript のモジュールは、コードを再利用可能な単位に編成してカプセル化する方法です。モジュールを使用すると、関連するコードをグループ化し、アプリケーションの異なる部分間で機能をインポートおよびエクスポートする方法を提供できます。モジュールはコードベースの編成と管理に役立ち、アプリケーションの保守と拡張が容易になります。 TypeScript では、export キーワードを使用してクラス、関数、変数、その他のエンティティをファイルからエクスポートし、import キーワードを使用してこれらのエンティティを別のファイルにインポートすることにより、モジュールを作成できます。また、export default キーワードを使用して、単一のエンティティをモジュールのデフォルトのエクスポートとしてエクスポートすることもできます。
// TypeScript でモジュールを作成する例を次に示します。
// ファイル: math.ts
export function add(x: number, y: number): number {
    return x + y;
}
export function subtract(x: number, y: number): number {
    return x - y;
}
// ファイル: app.ts
import { add, subtract } from "./math";
console.log(add(5, 3)); // Output: 8
console.log(subtract(5, 3)); // Output: 2
// この例では、加算と減算の 2 つの関数をエクスポートする math.ts という名前のモジュールを作成しました。次に、これらの関数を app.ts という名前の別のファイルにインポートし、それらを使用して加算および減算演算を実行します。
// TypeScript はエクスポートのデフォルト構文もサポートしており、単一のエンティティをモジュールのデフォルトのエクスポートとしてエクスポートできます。 TypeScript でエクスポートのデフォルトを使用する例を次に示します。
// ファイル: math.ts
function multiply(x: number, y: number): number {
    return x * y;
}
export default multiply;
// ファイル: app.ts
import multiply from "./math";
console.log(multiply(5, 3)); // Output: 15
// この例では、単一関数乗算をデフォルトのエクスポートとしてエクスポートする math.ts という名前のモジュールを作成しました。
// 次に、import ... from 構文を使用してこの関数を app.ts という名前の別のファイルにインポートし、それを使用して乗算演算を実行します。
// TypeScript は、export * 構文もサポートしており、モジュールからすべてのエンティティをエクスポートできます。 TypeScript での import * の使用例を次に示します。
// ファイル: math.ts
export function add(x: number, y: number): number {
    return x + y;
}
export function subtract(x: number, y: number): number {
    return x - y;
}
// ファイル: app.ts
import * as math from "./math";
console.log(math.add(5, 3)); // Output: 8
console.log(math.subtract(5, 3)); // Output: 2
// この例では、加算と減算の 2 つの関数をエクスポートする math.ts という名前のモジュールを作成しました。次に、import * as 構文を使用して、このモジュールからすべてのエンティティを app.ts という名前の別のファイルにインポートし、それらを使用して加算および減算の操作を実行します。
```