# mypkg

![test](https://github.com/Nao107010/mypkg/actions/workflows/test.yml/badge.svg)

* このリポジトリはROS2のパッケージです。
* ROS2を未インストールの方はインストールをお願いします。
* インストール完了後、リポジトリをワークスペースにクローンしてください。
```
$ git clone https://github.com/Nao107010/mypkg.git
```

# talker・listener
このノードを機能させるにはターミナルが2つ必要です。

まず、talkerはcountupというトピックを通じ、16ビットの符号付き整数型のメッセージを送ります。

その後、listener側がtalkerが送ってきた16ビットの符号付整数型のメッセージを順番に受信した通りに、エディタへと出力します。

無限ループする使用になっているので、止めたい場合は強制的に終了させてください。

## talker・listenerの実行例
今回の例では1つ目のターミナルをtalker側、2つ目をlistener側とします。
出力結果はターミナル2の方に出ます。

* ターミナル1(入力)
```
$ ros2 run mypkg talker
```
* ターミナル2(入力)
```
$ ros2 run mypkg listener
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
(以下省略)
```
# launchファイル
このファイルにあるtalk_listen.launchは複数のノードを一度に立ち上げるものとなっています。

## launchファイルの実行例

```
$ ros2 launch mypkg talk_listen.launch.py

[INFO] [talker-1]: process started with pid [410]
[INFO] [listener-2]: process started with pid [412]
[listener-2] [INFO] [1672342664.266903500] [listener]: Listen: 0
[listener-2] [INFO] [1672342664.747423900] [listener]: Listen: 1
[listener-2] [INFO] [1672342665.247433700] [listener]: Listen: 2
[listener-2] [INFO] [1672342665.748210900] [listener]: Listen: 3
[listener-2] [INFO] [1672342666.248159600] [listener]: Listen: 4
[listener-2] [INFO] [1672342666.748484100] [listener]: Listen: 5
[listener-2] [INFO] [1672342667.247912400] [listener]: Listen: 6
[listener-2] [INFO] [1672342667.747910700] [listener]: Listen: 7
[listener-2] [INFO] [1672342668.247886700] [listener]: Listen: 8
[listener-2] [INFO] [1672342668.747972200] [listener]: Listen: 9
[listener-2] [INFO] [1672342669.247801700] [listener]: Listen: 10
(以下省略)
```

# 動作確認済み環境
以下の環境で動作確認がされています。
* Ubuntu 22.04
* ROS2 humble

# ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます.
* © 2022 Naoto Sato

