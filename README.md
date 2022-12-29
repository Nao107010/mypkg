# mypkg
このリポジトリは未来ロボティクス学科のロボットシステム学の授業の課題で作ったものをあげるためのものです。

![test](https://github.com/Nao107010/mypkg/actions/workflows/test.yml/badge.svg)

* このリポジトリはROS2のパッケージなので、未インストール方はインストールをお願いします。
* ROS2インストール後、以下のようにリポジトリをクローンし、mypkgへ移動してください。
```
$ git clone https://github.com/Nao107010/mypkg.git
$ cd mypkg
```

* 今回使用するノードのtalker・listenerはさらにmypkgへと移動した先、talker_listener.launchはlaunchへと移動した先にあります。

# talker・listener
このノードを機能させるにはターミナルが2つ必要です。
まず、talkerはcountupというトピックを通じ、Int16型のメッセージを送ります。
その後、listener側がtalkerが送ってきたInt16型のメッセージを順番に受信した通りに、エディタへと出力します。

## talker・listenerの実行例
今回の例では1つ目のターミナルをtalker側、2つ目をlistener側とします。

* ターミナル1
```
$ ros2 run mypkg talker
```
* ターミナル2
```
$ros2 run mypkg listener
```




# 動作確認済み環境
以下の環境で動作確認がされています。
* OS Windows10
* Ubuntu 20.04

# ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます.
* © 2022 Naoto Sato

