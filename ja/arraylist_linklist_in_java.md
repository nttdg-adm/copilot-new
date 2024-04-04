---
title: "JavaのArrayList、LinkedListをGitHub Copilotを使用して学ぶ"
description: "JavaのArrayList、LinkedListをGitHub Copilotを使用して学ぶ"
category: general
platforms: [copilot, copilot-chat]
level: lv3
---

## JavaのArrayList、LinkedListをGitHub Copilotを使用して学ぶ
[<img src="https://img.shields.io/badge/Lv3-Mature_Best_Practice-brightgreen">](https://github.com/orgs/AI-Native-Development/projects/1/)

### 説明
コレクションは、オブジェクトの単位であり、グループを表します。
Javaのコレクションフレームワークは、多くのインターフェースとクラスを提供しています。`java.util`パッケージには、コレクションフレームワークのすべてのクラスとインターフェースが含まれています。

    Iterable
        ├── Collection
                ├── List
                │   ├──  ArrayList
                │   ├──  LinkedList

上記の階層図では、Iterable、Collection、Listはインターフェースであり、ArrayListとLinkedListはクラスです。
ListインターフェースはCollectionインターフェースの子インターフェースです。順序付けられたオブジェクトのコレクションを格納するリスト型のデータ構造を抑制します。重複した値を持つことができます。

ListインターフェースはArrayList、LinkedListのクラスによって実装されています。
Listインターフェースを実装するクラスは以下のとおりです。
- ArrayList
    #### 説明: 
    ArrayListは、Listインターフェースを使用して実装されたJavaのクラスです。ArrayListは配列のようなものですが、サイズ制限はありません。arrayList上で実行できる多くの操作があります。GitHub Copilotを使用してarrayListの宣言や操作を行うことができます。
    リストをトラバースする方法は多くあります。GitHub Copilotはそれに関する提案を行うことができます。例えば、`//イテレータを使用してリストをトラバースする`というコメントを書くと、イテレータを使用したトラバースの実装を提案してくれます。また、実装が完了すると、リストのトラバース方法に関するコメントの提案も行ってくれます。

    #### 例
    - **演習1**
        ##### 入力コード
        ```java
        import java.util.*;

        public class ArrayListExample {
        public static void main(String[] args) {
        // ArrayListの例を作成して表示します。
        }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.*;

        public class ArrayListExample {
            public static void main(String[] args) {
            //  ArrayListの例を作成して表示します。
            ArrayList<String> cars = new ArrayList<String>();
            cars.add("Volvo");
            cars.add("BMW");
            cars.add("Ford");
            cars.add("Mazda");
            System.out.println(cars);
            }
        }
        ```
    - **演習2**
        ##### 入力コード
        ```java
        import java.util.*;

        public class ArrayListExample {
        public static void main(String[] args) {
        // ArrayListの例を作成し、操作を行い、表示します。
        ArrayList<String> cars = new ArrayList<String>();
        cars.add("Volvo");
        cars.add("BMW");
        cars.add("Ford");
        cars.add("Mazda");
        System.out.println(cars);
        // イテレータを使用してリストをトラバースする
        }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.*;

        public class ArrayListExample {
            public static void main(String[] args) {
            //  ArrayListの例を作成して表示します。
            ArrayList<String> cars = new ArrayList<String>();
            cars.add("Volvo");
            cars.add("BMW");
            cars.add("Ford");
            cars.add("Mazda");
            System.out.println(cars);
            // イテレータを使用してリストをトラバースする
            Iterator<String> it = cars.iterator();
            while(it.hasNext()){
                System.out.println(it.next());
            }
            // forループを使用してリストをトラバースする
            for(int i=0;i<cars.size();i++){
                System.out.println(cars.get(i));
            }
            // for eachループを使用してリストをトラバースする
            for(String i:cars){
                System.out.println(i);
            }  
            // forEach()メソッドを使用してリストをトラバースする
            cars.forEach((n) -> System.out.println(n));
            // forEachRemaining()メソッドを使用してリストをトラバースする
            Iterator<String> it1 = cars.iterator();
            it1.forEachRemaining((n) -> System.out.println(n));
            // listIterator()メソッドを使用してリストをトラバースする
            ListIterator<String> it2 = cars.listIterator();
            while(it2.hasNext()){
                System.out.println(it2.next());
            }
            }
        }
        ```
- LinkedList
    #### 説明: 
    JavaのLinkedListクラスは、要素を格納するために双方向リンクリストを使用します。
    LinkedListクラスはArrayListとほぼ同じです。
    多くの場合、ArrayListはランダムなアイテムへのアクセスが必要なため、より効率的ですが、LinkedListは特定の操作をより効率的に行うためのいくつかのメソッドを提供します。GitHub Copilotを使用すると、ArrayListにはないメソッドを取得できます。`//arraylist にないリンク リストのメソッドの例を示します`というコメントを書くと、`addFirst()、addLast()、removeFirst()`などのメソッドの提案が表示されます。

    #### 例
    - **演習1**
        ##### 入力コード
        ```java
        import java.util.*;

        public class LinkedListExample {
        public static void main(String[] args) {
            // 車のブランド名を格納するLinkedListオブジェクトであるcarsを作成します
        }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.*;

        public class LinkedListExample {
            public static void main(String[] args) {
                // 車のブランド名を格納するLinkedListオブジェクトであるcarsを作成します
                LinkedList<String> cars = new LinkedList<String>();
                // リストの末尾に要素を追加します
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");
                // リストを表示します
                System.out.println(cars);
            }
        }
        ```
    - **演習2**
        ##### 入力コード
        ```java
        import java.util.*;

        public class LinkedListExample {
            public static void main(String[] args) {
                // 車のブランド名を格納するLinkedListオブジェクトであるcarsを作成します
                LinkedList<String> cars = new LinkedList<String>();
                // リストの末尾に要素を追加します
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");
                // リストを表示します
                System.out.println(cars);

                // Arraylist にないリンク リストのメソッドの例を示します
            }
        }
        ```
        
        ##### Copilotによる提案結果

        ```java
        import java.util.*;

        public class LinkedListExample {
            public static void main(String[] args) {
                // 車のブランド名を格納するLinkedListオブジェクトであるcarsを作成します
                LinkedList<String> cars = new LinkedList<String>();
                // リストの末尾に要素を追加します
                cars.add("Volvo");
                cars.add("BMW");
                cars.add("Ford");
                cars.add("Mazda");
                // リストを表示します
                System.out.println(cars);

                // ArrayListにはないLinkedListのメソッドの例を示します
                // リストの末尾に要素を追加します
                cars.addLast("Honda");
                // リストを表示します
                System.out.println(cars);
                // リストの最後の要素を削除します
                cars.removeLast();
                // リストを表示します
                System.out.println(cars);
            }
        }
        ```