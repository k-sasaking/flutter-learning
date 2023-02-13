# アプリの作成

本性では、複数のボタンが押されたときの処理をするアプリを作ります。

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

  void _changeText(int number) {
    setState(() {
       String result = "";
       // ここから課題の処理を追加
       if(number == 0){
         result = "ボタンAが押されました";
       }
       else if(number == 1){
         result = "ボタンBが押されました";
       }
       else {
         result = "ボタンCが押されました";
       }
       // ここまで課題の処理を追加
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
             TextButton(
              child: const Text('ボタンA'),
              onPressed: () {
                _changeText(0);
              },
            ),
             TextButton(
              child: const Text('ボタンB'),
              onPressed: () {
                _changeText(1);
              },
            ),
             TextButton(
              child: const Text('ボタンC'),
              onPressed: () {
                _changeText(2);
              },
            ),
          ],
        ),
      ),
    );
  }
}
```

まずは、動かしてみましょう！

ボタンを押すと、「ボタン A が押されました」 に変わります。

## 課題１：クイズ アプリ

問題文を出し、押されたボタンが正解の場合は、「正解」。
ハズレの場合は、「ハズレ」と表示するプログラムを作りましょう。

- 「ここにボタンが押される前の文字を書く:before 」に問題文を作りなさい。（例）日本一大きい山は？
- ボタン A,ボタン B、ボタン C の文字を回答候補にしなさい。例）浅間山、富士山、赤城山
- 「ボタン A が押されました」「ボタン B が押されました」「ボタン C が押されました」のところを「正解」、「ハズレ」にしなさい。

## 課題 2: じゃんけんアプリ 1

グー、チョキ、パーのボタンを作成し、そのボタンが押されたら、「グーが押されました」のようなプログラムを作成しなさい。

- 「ここにボタンが押される前の文字を書く:before 」を「じゃんけんをします」に変える
- ボタン A,ボタン B、ボタン C の文字を「グー」「チョキ」「パー」
- 「ボタン A が押されました」「ボタン B が押されました」「ボタン C が押されました」のところを「グーが押されました」「チョキが押されました」「パーが押されました」にしなさい。

## 課題 3: じゃんけんアプリ 2

ボタンを押したら、じゃんけんの対戦ができるアプリを作りなさい。

例）グーのボタンが押されたとき、ランダムな手を用意して、「あなたの勝ち」「あいこ」「あなたの負け」のように表示する。

- ランダムな数を作り、0 の時は、「グー」、1 の時は「チョキ」、2 の時は「パー」となるようにし、「コンピュータの手は〇〇です」と表示しなさい。
- ランダムな数と引数 number が同じの場合は、「コンピュータの手は、〇〇です。あいこです。」と表示しなさい。
- コンピューターの手と引数 number の手を比べて、勝ちの場合は、「コンピュータの手は、〇〇です。あなたの勝ちです」と表示しなさい。
- それ以外の時は、「コンピュータの手は、〇〇です。あなたの負けです」と表示しなさい。
