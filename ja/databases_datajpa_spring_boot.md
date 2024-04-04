---
title: "GitHub Copilot を使用した Spring Boot のデータベースと DataJPA"
description: "GitHub Copilotを使用したSpring BootでのデータベースとDataJPAの利用方法"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## GitHub Copilot を使用した Spring Boot のデータベースと DataJPA
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/
 
### 説明
Spring BootアプリケーションのリレーショナルデータベースにはMySQL、PostgreSQL、Oracle、Microsoft SQL Serverが含まれます。

Spring Bootを使用すると、さまざまなデータベースに接続し、Spring Data JPAを使用してデータベースにアクセスすることができます。Spring Bootは、MySQL、PostgreSQL、Oracle、Microsoft SQL Serverを含むさまざまなデータベースに接続するために使用できます。

**使用するタイミング**: アプリケーションが強力なデータの整合性、ACIDトランザクション、データエンティティ間の明確な関係を必要とする場合、MySQLのようなリレーショナルデータベースが最適な選択肢となるでしょう。

### Spring Bootでデータベースを作成する方法は？
ステップバイステップのSpring Bootプロジェクトの更新

- ステップ1 - pom.xmlにデータベースコネクタの依存関係を追加します。
- ステップ2 - pom.xmlからH2の依存関係を削除します。または、少なくともテストのスコープにします。
- ステップ3 - MySQLデータベースをセットアップします。
- ステップ4 - データベース接続をセットアップします。
- ステップ5 - 再起動して完了です。
- ついにリリースされました。

**Java Persistence API（JPA）**は、Javaでデータベースにアクセスするための標準的なインターフェースであり、Javaクラスとデータベーステーブルの自動マッピングを提供します。

GitHub Copilotは、自然言語に基づいてコードスニペットや提案を生成することで、Spring Bootの理解を支援することができます。これは、エンティティやリポジトリ、クエリメソッドの定義などのタスクにおいて、より直感的な方法でSpring JPAの概念を理解しやすくするのに役立ちます。

### 例

## 入力コード
```java
package com.example.demo;

import org.springframework.web.bind.annotation.RestController;

@RestController
public class index {
    // ユーザーを追加するためにSpringJPA操作を実行します
    
    
}
```

## Copilotによる提案結果
```java
package com.example.demo;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class index {
    // ユーザーを追加するためにSpringJPA操作を実行します
    @Autowired
    private UserRepository userRepository;

    @RequestMapping("/")
    public String index() {
        User user = new User();
        user.setName("John");
        user.setRole("Admin");
        userRepository.save(user);
        return "ユーザーが追加されました";
    }
}
```
