---
title: "GitHub Copilotを使用したSpring BootでのRESTful API"
description: "GitHub Copilotを使用したRESTful API"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## GitHub Copilotを使用したSpring BootでのRESTful API
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### 説明
表現状態転送（REST）は、Webサービスの作成に使用するための一連の制約を定義するソフトウェアアーキテクチャスタイルです。RESTのアーキテクチャスタイルに準拠したWebサービスは、インターネット上のコンピュータシステム間で相互運用性を提供します。

Spring Bootを学ぶ最良の方法は、REST APIを開発することです。
さらに、これらはマイクロサービスで使用されるか、他のアプリケーションによって消費されます。REST APIでは、次のことを学ぶことができます：

- HTTPメソッド：POST、GET、PUT、DELETE、OPTIONS、TRACE
- HTTPステータスコード：1.X.X、2.X.X、3.X.X、4.X.X、5.X.X

### 例
この例では、単一のエンドポイント/api/helloを公開するシンプルなRESTful APIを作成します。

クライアントがこのエンドポイントにGETリクエストを送信すると、APIは文字列「こんにちは、世界！」を返します。

## 入力コード
```java
@SpringBootApplication
public class DemoApplication {

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}

@RestController
@RestMapping("/api")
public class DemoController {
    // 基本認証を実行する...

    @GetMapping("/hello")
    public String hello(){
        return "こんにちは、世界！";
    }
}
```

## Result Suggested by Copilot
```java
@SpringBootApplication
public class DemoApplication {

    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }

}

@RestController
@RestMapping("/api")
public class DemoController {
   // 基本認証を実行する...

    @GetMapping("/hello")
    public String hello(){
        return "こんにちは、世界！";
    }
}
```



