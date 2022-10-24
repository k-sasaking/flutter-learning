# 乱数

本日は、乱数について学んでいきましょう。

乱数とは、ランダムな数です。

プログラムによってランダムな数を作ることができます。

乱数は、ゲームなどのガチャの確率などの計算などにも使われています。

## 乱数の使い方

まずは、乱数を作るプログラムを実行してみましょう。

0,1,2,3,4のいずれかのランダムの数を出すプログラムを実行してみましょう。

```
import 'dart:math' as math;

void main() {
  var rand = new math.Random();
  print(rand.nextInt(5));
}
```

想定される結果は、0,1,2,3,4のいずれかの数字が表示されます。


乱数の使い方は以下の通りに使います。


① import文を一番上に記載する。

```
import 'dart:math' as math;
```


② 乱数を呼び出す。

```
var rand = new math.Random();
rand.nextInt(5)
```


③nextIntの使い方

nextIntの中の数字は、何個のランダムな数を作るかを示しています。


例えば、0,1,2を出したい場合は、nextInt(3)となります。


0から9の値を出したいときは、nextInt(10)とします。



## 演習9-1


プログラムを変更して、0から99のランダムな数を出すプログラムを作成しなさい。

想定結果

```
import 'dart:math' as math;

void main() {
  var rand = new math.Random();
  print(rand.nextInt(5));
}
```




## 演習9-2

プログラムを変更して、変数handが0の時は、グー。1の時は、チョキ。2の時は、パーと表示しなさい。


想定結果

```
import 'dart:math' as math;

void main() {
  var rand = new math.Random();
  int hand = rand.nextInt(3);


}
```



## 演習9-3

0から99のランダムな数をだして、50以上なら「当たり」それ以外なら「ハズレ」と表示するプログラムを作成しなさい。

また、その処理を３回繰り返しなさい。


想定結果

```
import 'dart:math' as math;

void main() {
  var rand = new math.Random();


}
```




