# 概要
ロボットシステム学の課題１です。　

中身はLEDを光らせるデバイスドライバです。

上田先生の授業で扱ったサンプルを実装しました。

下のリンクが授業のスライド資料のURLです。

https://ryuichiueda.github.io/robosys2020/lesson7_device_driver.html#/

（このリポジトリが1-REDなのは誤爆です。許してください）

# 動作環境
・Raspberry Pi4 Model BはノートPC（Windows10)を経由してインターネット接続してます。

（Raspberry Pi4を今後ラズパイと略すことがあります）

直接ラズパイとwifiルーターをLANで接続してインターネットに繋いでもできます。

・WSL2のubunu20.04.3 LTSを使用してます。

また、ラズパイもubunu20.04.3 LTSです。



・ノートPCを経由してインターネット接続する方法のリンク

　https://twitter.com/ryuichiueda/status/1178124814076149761


・ラズパイにubuntuをインストールする方法のリンク

　https://twitter.com/ryuichiueda/status/1250644188992962560


# 使用した物
・Raspberry Pi4 Model B　× 1

・マイクロSDカード（ラズパイ用） × 1

・ラズパイ用の電源（端子はtype-c) × 1

・ノートPC（Windows10 / 64bit) × 1

・wifi環境（私は2.4GHzで通信）

・ブレッドボード × 1

・抵抗(220Ω） × 1

・ジャンパー × 2

・LED × 1


# 回路を作成
ここに写真
![37511](https://user-images.githubusercontent.com/93900927/148146640-254ad255-16d2-4b06-98e7-1cb89e91c49b.jpg)


# デバイスドライバをインストール


# LED点灯


# LED消灯


# デバイスドライバをアンインストール


# 実際にLEDを光らせる


# ライセンス
GPL 3.0
