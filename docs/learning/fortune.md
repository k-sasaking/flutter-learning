# 配列

本日は、配列について学んでいきましょう。

配列とは、複数の変数を１つにまとめて順番に並べたものです。

## 配列の使い方


まずは、文字列の配列を作ってみましょう。


```
void main() {
  List<String> students = ["山田", "田中", "中山", "山川"];
  print(students);
}

```

想定される結果

```
[山田, 田中, 中山, 山川]
```

　
配列の値は、以下のように、要素で指定することができます。

```
List<String> 変数名 = ["要素1", "要素2", "要素3"];
```

　

　
　

また、配列の型は以下のように指定することで決まります。

```
 List<型>
```

型には、String, int, booleanなどが入ります。



例）
```
List<int> scores = [50, 60, 80, 100];
```




## 配列の要素の取り出し


配列は、数字を指定することで何番目の値を取り出すかを指定することができます。

順番は、0から数えて、0番目,1番目,2番目,3番目,4番目...となります。

```
void main() {
  List<String> fruits = ["Apple", "Grape", "Orange", "Peach"];
  print(fruits[0]);
  print(fruits[3]);
}
```


想定される結果

```
Apple
Peach
```

今回で言うと、0番目:APple、1番目:Grape、2番目:Orange、3番目:Peachなので、

0番目と3番目はそれぞれ、AppleとPeachになります。


このように、[番目]で数字を入れることで、取り出すことができます。



想定されていない番号を指定するとエラーになります。

```
void main() {
  List<String> fruits = ["Apple", "Grape", "Orange", "Peach"];
  print(fruits[0]);
  print(fruits[10]);  //エラーになる。
}
```

以下のメッセージは、番号が範囲外にあると言う意味です。
```
Index out of range
```

## 配列の値の更新


配列は、n番目のように指定することで、それを変数と同じように扱うことができます。

つまり、そこに値を代入することもできます。

以下のプログラムを実行してみましょう。


```
void main() {
  List<String> fruits = ["Apple", "Grape", "Orange", "Peach"];
  
  print(fruits);
  
  fruits[0] = "Pineapple";

  print(fruits);

}
```



## 演習10-1

以下のプログラムを変更して想定結果になるように変更しなさい。


```
void main() {
  List<String> members = ["田中", "遠藤", "山根", "本田"];
  
  print(members);
  
  // ここにプログラムを変更

  print(members);


}
```

```
["田中", "遠藤", "山根", "本田"]
["田中", "遠藤", "山根", "森田"]
```



## 演習10-2

以下のプログラムを変更し、ランダムに「大吉」「中吉」「小吉」「吉」「末吉」「凶」「大凶」のいずれかが出るプログラムを書きなさい。


```
import 'dart:math' as math;

void main() {
  List<String> results = []; // ここに配列を定義

  var rand = new math.Random();
  int number = rand.nextInt(7);

  print(/*ここにプログラムを追加*/);

}
```



## 演習10-3


10-2のプログラムを参考に、ランダムに「グー」「チョキ」「パー」が出るプログラムを作成しなさい。



