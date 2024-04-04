---
title: "GitHub Copilotを使用したSpring BootでのCRUD操作"
description: "GitHub Copilotを使用したCRUD操作のシンプルなコード補完"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したSpring BootでのCRUD操作の例
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
CRUDは、ソフトウェアアプリケーションが実行できる基本的な4つの操作を指します。
 - 作成（Create）
 - 読み取り（Read）
 - 更新（Update）
 - 削除（Delete）

ユーザーはデータを作成できる必要があり、データにアクセスしてデータを読み取ることができ、データを更新または編集でき、データを削除できる必要があります。

CRUDの各アクロニムの各文字には、対応するHTTPリクエストメソッドがあります。

                |  CRUD OPERATION  |  HTTP REQUEST METHOD  |
                |      Create      |       POST            |
                |      Read        |       Get             |
                |      Update      |       PUT & Patch     |
                |      Delete      |       Delete          |
 
GitHub Copilotは、Spring Bootアプリケーションで「作成」操作を生成できます。開発者は、エンティティの作成または作成操作を行う意図を説明するコメントや部分的なコードスニペットを提供することで開始できます。

また、GitHub Copilotは、正しい指示が与えられた場合に提案を提供します。
開発者は「Spring Bootで新しいユーザーを作成する」というコメントを付けています。

### 例

#### 入力コード

```java
@PostMapping("/users")
public ResponseEntity<User> createUser
(@RequestBody User user){
    //新しいユーザーを作成して表示する
}
```

#### Copilotが提案した結果
```java
           
            @PostMapping("/users")
            public ResponseEntity<User> createUser(@RequestBody User user) {
                 //新しいユーザーを作成して表示する
                User createdUser = userRepository.save(user);
                return ResponseEntity.ok(createdUser);
            }
```
開発者は、GitHub Copilotに残りのCRUD操作を尋ねることもできます。Copilotは適切な解決策を提案するコードを示します。

>## 練習:-
1. このアクティビティで同じ読み取り操作を試して、Copilotによるより信頼性と効率性の高い方法を尋ねてみてください。
2. Copilotを使用して、ユーザーの削除操作または削除を行ってみてください。
