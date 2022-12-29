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
よって出力結果はターミナル2の方に出ます。

* ターミナル1
```
$ ros2 run mypkg talker
```
* ターミナル2
```
$ros2 run mypkg listener
```
* ターミナル2(出力結果)
```
[INFO] [1672339755.782609300] [listener]: Listen: 0
[INFO] [1672339756.270829500] [listener]: Listen: 1
[INFO] [1672339756.769829400] [listener]: Listen: 2
[INFO] [1672339757.270826700] [listener]: Listen: 3
[INFO] [1672339757.769282700] [listener]: Listen: 4
[INFO] [1672339758.270047300] [listener]: Listen: 5
[INFO] [1672339758.770658500] [listener]: Listen: 6
[INFO] [1672339759.269420100] [listener]: Listen: 7
[INFO] [1672339759.769975100] [listener]: Listen: 8
[INFO] [1672339760.270004400] [listener]: Listen: 9
[INFO] [1672339760.770247600] [listener]: Listen: 10
(以下略)
```



# 動作確認済み環境
以下の環境で動作確認がされています。
* OS Windows10
* Ubuntu 20.04

# ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます.
* © 2022 Naoto Sato

