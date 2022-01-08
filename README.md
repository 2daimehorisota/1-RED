# 概要
ロボットシステム学の課題１です。　

中身はLEDを光らせるデバイスドライバです。

上田先生の授業で扱ったコードを実装しました。



下のリンクが授業のスライド資料のURLです。

https://ryuichiueda.github.io/robosys2020/lesson7_device_driver.html#/



# 動作環境
・Raspberry Pi4 Model BはノートPC（Windows10)を経由してインターネット接続してます。

（Raspberry Pi4を今後ラズパイと略すことがあります）

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


<img src="https://user-images.githubusercontent.com/93900927/148147915-54790d3e-b307-44dc-bcaf-dc47ea65cf30.jpg" width="600px">

実際の回路です。

22ピン（GPIO25）→　LED　→　抵抗（220Ω） →　39ピン（GND）

をジャンパー線とブレッドボードを用いて回路を作ります。

LEDのアノード（足が長い方)を22ピンの方に指すようにしてください。



# 実際の回路の様子

22ピンを1ピン（3.3V　PWR）に変えると回路が出来てるかテストできます。

<img src="https://user-images.githubusercontent.com/93900927/148147926-fa443a37-35db-4ebc-9f90-83efd19ad422.jpg" width="600px">


LEDが光れば回路が出来ています。

# デバイスドライバをインストール

    $git clone git@github.com:2daimehorisota/1-RED.git

    $cd 1-RED　//1-REDへ移動
    
    $cd myled　//myledへ移動

    $ls  //Makefileとmyled.cがあるか確認
    
    $make
    
    $sudo insmod myled.ko
    
    $sudo chmod 666 /dev/myled0

これで準備完了です。
# LED点灯
    $echo 1 > /dev/myled0

# LED消灯
    $echo 0 > /dev/myled0

# デバイスドライバをアンインストール
    $sudo rmmod myled

    $make clean

これでアンインストールは完了です。

# 実際にLEDを光らせる



https://user-images.githubusercontent.com/93900927/148161667-d3a722a9-95df-4fb0-848a-afcfec5c9bed.mp4

https://www.youtube.com/watch?v=jcV5P24OaPI


# COPYING


GNU General Public License v3.0

https://www.gnu.org/licenses/gpl-3.0.ja.html
