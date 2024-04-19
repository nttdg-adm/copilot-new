---
title: "GitHub Copilotを使用したスレッドプールの種類"
description: "GitHub Copilotを使用したスレッドプールの種類"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## GitHub Copilotを使用したJavaのスレッドプールの種類
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
データベースやWebサーバーなどのサーバープログラムは、複数のクライアントからのリクエストを繰り返し実行します。これには、リクエストが到着するたびに新しいスレッドを作成する多数の小さなタスクが含まれています。このアプローチは実装が簡単に見えますが、重要な欠点があります。
このアプローチでは時間がかかり、システムのメモリを枯渇させる可能性があります。そのため、作成されるスレッドの数を制限する必要があります。
スレッドプールは、以前に作成されたスレッドを再利用して現在のタスクを実行し、スレッドのサイクルオーバーヘッドとリソースの無駄遣いの問題に対する解決策を提供します。
Javaのスレッドプールは、Executorフレームワークによって管理されるスレッドのグループです。Executorフレームワークは、Executorインターフェースを中心に展開されており、そのサブインターフェースであるExecutorServiceとクラスであるThreadPoolExecutorが実装されています。Executorを使用することで、実行するRunnableオブジェクトを実装するだけで済みます。
Executorフレームワークは、スレッドを手動で作成および管理する必要なく、タスクを実行する方法を提供します。これにより、パフォーマンスとリソースの利用率が向上します。

スレッドプールの種類：
1. 固定スレッドプール
2. キャッシュスレッドプール
3. スケジュールドスレッドプール

GitHub Copilotは、指示に従ってスレッドプールを作成するのに役立ちます。
また、ExecutorsパッケージやExecutorServiceのインポートが追加されていない場合、エディターにエラーが表示されます。GitHub Copilotは、これらのエラーを修正するのに役立ちます。
#### 例
- **演習1 - 固定スレッドプール**
##### 入力コード
```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
/**
 * FixedThreadPoolExample
 */
public class FixedThreadPoolExample {
    public static void main(String[] args){
        // Create a fixed thread pool with 5 threads
        }
    }
// create a task class that implements Runnable interface
// sleep for 1000 milliseconds
// print the thread name and the task name
```

##### Copilotが提案した結果

```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

/**
 * FixedThreadPoolExample
 */
public class FixedThreadPoolExample {

    public static void main(String[] args){
        // 5つのスレッドを持つ固定スレッドプールを作成する
        ExecutorService executor = Executors.newFixedThreadPool(5);
        // 10個のタスクをエグゼキューターサービスに送信する
        for (int i = 0; i < 10; i++) {
            Runnable worker = new WorkerThread("task" + i);
            executor.execute(worker);
        }
        executor.shutdown();
        
    }
}
// Runnableインターフェースを実装するタスククラスを作成する
// 1000ミリ秒スリープする
// スレッド名とタスク名を表示する
class WorkerThread implements Runnable {
    private String taskName;
    public WorkerThread(String taskName) {
        this.taskName = taskName;
    }
    public void run() {
        System.out.println(Thread.currentThread().getName() + " 開始。タスク = " + taskName);
        processTask();
        System.out.println(Thread.currentThread().getName() + " 終了。タスク = " + taskName);
    }
    private void processTask() {
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}
```
- **演習2 - キャッシュスレッドプール**
##### Input Code
```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
/**
 * CachedThreadPoolExample
 */
public class CachedThreadPoolExample {
    public static void main(String[] args){
        // 5つのスレッドを持つキャッシュスレッドプールを作成する
        ExecutorService executor = Executors.newCachedThreadPool();
        // 10個のタスクをエグゼキューターサービスに送信する
        for (int i = 0; i < 10; i++) {
            Runnable worker = new WorkerThread("task" + i);
            executor.execute(worker);
        }
        executor.shutdown();
    }
}

// Runnableインターフェースを実装するタスククラスを作成する
// 1000ミリ秒スリープする
// スレッド名とタスク名を表示する
```

##### Copilotが提案した結果

```java
/**
 * CachedThreadPoolExample
 */
public class CachedThreadPoolExample {

    public static void main(String[] args) {
        // キャッシュスレッドプールを作成する
        ExecutorService executor = Executors.newCachedThreadPool();
        // 10個のタスクをエグゼキューターサービスに送信する
        for (int i = 0; i < 10; i++) {
            Runnable worker = new WorkerThread("task" + i);
            executor.execute(worker);
        }
        executor.shutdown();

    }
}

// Runnableインターフェースを実装するクラスを作成する
// 1000ミリ秒スリープする
// スレッド名とタスク名を表示する
class WorkerThread implements Runnable {
    private String taskName;

    public WorkerThread(String taskName) {
        this.taskName = taskName;
    }

    public void run() {
        System.out.println(Thread.currentThread().getName() + " 開始。タスク = " + taskName);
        processTask();
        System.out.println(Thread.currentThread().getName() + " 終了。タスク = " + taskName);
    }

    private void processTask() {
        try {
            Thread.sleep(1000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}
```