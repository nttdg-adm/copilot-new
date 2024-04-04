---
title: "GitHub Copilotを使用したSpring Bootでのページネーションとソート"
description: "GitHub Copilotを使用したページネーションとソート"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
 
## GitHub Copilotを使用したSpring Bootでのページネーションとソート
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)
 
### 説明
ページネーションは、大量のデータをより管理しやすいチャンクに分割するための技術です。ユーザーは、一度に表示されるレコードのサブセットを表示することで、データをナビゲートすることができます。これは、大規模なデータセットを扱う場合や、データをユーザーフレンドリーな方法で表示する場合に特に有用です。

Spring Bootのコンテキストでは、ページネーションは、クエリパラメータ、ページオブジェクト、またはサードパーティのライブラリなど、さまざまな技術を使用して実装することができます。ページサイズ（ページごとのレコード数）と現在のページ番号を指定することが含まれます。バックエンドアプリケーションは、これらのパラメータに基づいて関連するデータのサブセットを取得し、クライアントに返します。

ページネーションは、特定のフィールドの昇順または降順など、特定の基準に基づいてデータを並べ替えることができるソートとしばしば組み合わせられます。これにより、アプリケーションに追加の柔軟性と使いやすさが提供されます。

GitHub Copilotは、Spring Bootアプリケーションでのページネーションとソートの実装に必要なコードを生成するのに役立ち、開発者の時間と労力を節約します。

GitHub Copilotに、ページネーションとソートのロジックを実装したコントローラの例を作成してもらいましょう：

### 例
```java
import com.example.repository.UserRepository;

@Controller
public class UserController {

    private final UserRepository userRepository;

    public UserController(UserRepository userRepository) {
        this.userRepository = userRepository;
    }

    // ユーザーリストに対してページネーションとソートを実行し、結果を返す
    
}
```

### GitHub Copilotによる提案
```java
import java.util.List;

import com.example.repository.UserRepository;
import org.springframework.http.HttpHeaders;
@Controller
public class UserController {

    private final UserRepository userRepository;

    public UserController(UserRepository userRepository) {
        this.userRepository = userRepository;
    }

    // ユーザーリストに対してページネーションとソートを実行し、結果を返す 
    @GetMapping("/users")
    public ResponseEntity<List<User>> getUsers(@RequestParam(defaultValue = "0") Integer pageNo,
                                               @RequestParam(defaultValue = "10") Integer pageSize,
                                               @RequestParam(defaultValue = "id") String sortBy) {
        List<User> list = userRepository.findAll(pageNo, pageSize, sortBy);
        return new ResponseEntity<List<User>>(list, new HttpHeaders(), HttpStatus.OK);
    }
    
}
```
