# アプリの作成

本性では、ボタンを押したら、文字が変わる機能を使って、アプリを作成していきます。

## Dartpad で flutter

以下のコードを dartpad にコピーして、実行してみましょう。

```
import 'package:flutter/material.dart';

Future<void> main() async => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      debugShowCheckedModeBanner: false,
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: const MyHomePage(title: 'Flutter Demo Home Page'),
    );
  }
}

class MyHomePage extends StatefulWidget {
  final String title;

  const MyHomePage({
    Key? key,
    required this.title,
  }) : super(key: key);
  @override
  _MyHomePageState createState() => _MyHomePageState();
}

//  2.Stateを継承したクラスを作る。
class _MyHomePageState extends State<MyHomePage> {
  String _text = "ここにボタンが押される前の文字を書く:before";

  void _changeText() {
    setState(() {
       String result = "";
       // ここに課題の処理を追加

       result = "ここにボタンが押された時の文字を書く:after";

      _text = result;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            const Text(
              'ここにアプリの説明を書く',
            ),
            Text(
              '$_text',
              style: Theme.of(context).textTheme.headline4,
            ),
          ],
        ),
      ),

      // ボタン操作に応じて_counterを増やす
      floatingActionButton: FloatingActionButton(
        // onPressedされると、_counter++され、setState()によってUIが再描画される。
        onPressed: _changeText,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ),
    );
  }
}
```

まずは、動かしてみましょう！

ボタンを押すと、before->after に変わります。

## 課題１：Hello World アプリ

- 「ここにアプリの説明を書く」に「ボタンを押すと文字が変わります」と記載しましょう
- 「ここにボタンが押された時の文字を書く:after」のところを「Hello World!!」に書き換えましょう。

ボタンのアイコンや、色などを変更したら完成です。

## 課題 2: くじ引きアプリ

- 「ボタンを押すと文字が変わります」に「くじを引きますか？」と記載しましょう
- 「ここにボタンが押された時の文字を書く:after」に「大当たり」「当たり」「ハズレ」がランダムに出るようにしましょう。

<a href="https://k-sasaking.github.io/flutter-learning/learning/dart9.html" traget="_blank">ランダムな数の出し方</a>

## 課題 3: 占いアプリ

- 「ボタンを押すと文字が変わります」に「占いをしますか？」と記載しましょう
- 「ここにボタンが押された時の文字を書く:after」に「大吉」「中吉」「小吉」「吉」「末吉」「凶」「大凶」がランダムに出るようにしましょう。

<a href="https://k-sasaking.github.io/flutter-learning/learning/dart9.html" traget="_blank">ランダムな数の出し方</a>

## 課題 4: じゃんけんアプリ

- 「ボタンを押すと文字が変わります」に「じゃんけんをしますか？」と記載しましょう
- 「ここにボタンが押された時の文字を書く:after」に「グー」「チョキ」「パー」がランダムに出るようにしましょう。
- if 文ではなく、配列を使って表現しましょう

<a href="https://k-sasaking.github.io/flutter-learning/learning/dart9.html" traget="_blank">ランダムな数の出し方</a>
<a href="https://k-sasaking.github.io/flutter-learning/learning/dart10.html" traget="_blank">配列の使い方</a>
