# DartPad でプログラミング

ここからは DartPad というオンラインプログラミング実行環境にてプログラムを書くやり方で Dart の基本文法をマスターします。

## DartPad とは？

DarPad は、オンライン上で Dart のプログラムを実行できる環境です。

[https://dartpad.dev/?](https://dartpad.dev/?){:target="\_blank"}

※アカウント作成をしなくても実行ができます。

## Dartpad

最初コードを実行してみよう！

```
void main() {
  for (int i = 0; i < 5; i++) {
    print('hello ${i + 1}');
  }
}

```

「▷ Run」ボタンを押すと Console の枠に結果が出てきます。

```
hello 1
hello 2
hello 3
hello 4
hello 5
```

このように、プログラムを記載して「Run」を押すことでプログラムを実行することができます。

## Console 出力

それでは、プログラムを以下のように変更して Run をしてみましょう。

```
void main() {
    print('hello world!!');
}
```

想定結果

```
hello world!!
```

このように、print(``)の中に書かれた文字が表示されるようになっています。

## 演習１

Console に自分の名前を出力してみましょう。
