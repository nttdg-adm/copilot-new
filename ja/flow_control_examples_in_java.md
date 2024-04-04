---
title: "GitHub Copilotを使用したJavaのフロー制御の例"
description: "GitHub Copilotを使用したJavaのフロー制御の構文を学ぶ"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---
## GitHub Copilotを使用したJavaのフロー制御の例
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
Javaにはさまざまな種類のフロー制御文があります。if-else文、forループ、whileループなどがあります。Javaとその構文が初めての場合、GitHub Copilotを使用して構文についてのアイデアを得ることができます。Googleで検索したり、他の場所からコピーする必要はありません。GitHub Copilotを使用して、構文やさまざまな要素を学ぶことができます。
Javaのif-else文の構文についてのアイデアがない場合、`//if-else 構文の例を教えてください`というコメントをJavaファイルに書くと、自動的に構文が生成されます。
また、if-else文で文字列変数を使用したい場合は、if-else文で変数を使用するように指示してください。適切な結果が得られます。

#### 例
- **演習1**
    ##### 入力コード
    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
           //ここにif-else文の例を教えてください
        }
    }
    ```

    ##### Copilotによる提案結果

    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
           //ここにif-else文の例を教えてください
           if (true) {
               System.out.println("これは真です");
           } else {
               System.out.println("これは偽です");
           }
        }

    }
    ```
- **演習2**
    ##### 入力コード
    ```java
    public class FlowControlExample {

    public static void main(String[] args) {
        //例1
       //ここにif-else文の例を教えてください
       if (true) {
           System.out.println("これは真です");
       } else {
           System.out.println("これは偽です");
       }

       //例2
       //以下のデータを使用して、if-else文の例を教えてください
        int a = 10;
        int b = 20;
    }
    ```
    
    ##### Copilotによる提案結果
    
    ```java
    public static void main(String[] args) {
        //例1
       //ここにif-else文の例を教えてください
       if (true) {
           System.out.println("これは真です");
       } else {
           System.out.println("これは偽です");
       }

       //例2
       //以下のデータを使用して、if-else文の例を教えてください
        int a = 10;
        int b = 20;
        if (a > b) {
            System.out.println("aはbより大きいです");
        } else {
            System.out.println("bはaより大きいです");
        }
    }
    ```
- **演習3**
    ##### 入力コード
    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
           //Javaにおける制御フロー文の例を示します
        }
    }
    ```

    ##### Copilotによる提案結果

    ```java
    public class FlowControlExample {

        public static void main(String[] args) {
        //Javaにおける制御フロー文の例を示します
        //If-Else
        int a = 10;
        int b = 20;
        if(a > b){
            System.out.println("aはbより大きいです");
        }else{ 
            System.out.println("bはaより大きいです");
        }
        //Switch
        int c = 10;
        switch(c){
            case 10:
                System.out.println("こんにちは、世界");
                break;
            default:
                System.out.println("こんにちは、世界");
        }
        //For
        for(int d = 0; d < 10; d++){
            System.out.println("こんにちは、世界");
        }
        //While
        int i = 0;
        while(i < 10){
            System.out.println("こんにちは、世界");
            i++;
        }
        //Do-While
        int j = 0;
        do{
            System.out.println("こんにちは、世界");
            j++;
        }while(j < 10);
        //Break
        for(int k = 0; k < 10; k++){
            if(k == 5){
                break;
            }
            System.out.println("こんにちは、世界");
        }
        //Continue
        for(int l = 0; l < 10; l++){
            if(l == 5){
                continue;
            }
            System.out.println("こんにちは、世界");
        }
        }

    }
    ```