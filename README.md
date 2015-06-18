# Arduino-DHT22-RTC-SPP
DHT22で測定した温度と湿度を無線でプッシュするArduino用プログラム


テストd

//
// DHT系のセンサを使って，温度と湿度を測定し，Bluetoothで送信するプログラム
// RTCを使って，一定時間間隔で測定と送信を実行する．
// 測定していない期間はArduinoはスリープ状態となり，
// RTCの割込みで処理が再開する
//


# 変更する場合

## RTC関係
//
// RTCからarduinoに割込みを上げる端子と割込み番号の指定
// 本当なら，割込み番号を入れたら端子も機種毎の切り替えを効かせたいが，とりあえず固定指定
//
// 手持ちのMega2560では，INT0,1が動作しなかったため，大きい番号の割込みを利用
#define INT_NUMBER 5
#define PIN_NUMBER 18
// UNOはINT0,1が動作するため，こちらを利用
//#define INT_NUMBER 0
//#define PIN_NUMBER 2




## デバッグ関係
以下の*define文*を有効にすると，シリアルにメッセージが
出力される．

`#define USE\_SERIAL`


