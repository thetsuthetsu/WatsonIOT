# IBM Watson IoT PlatformのMQTT-Javaクライアント構築例
## 参考
* https://www.ibm.com/developerworks/jp/cloud/library/cl-mqtt-bluemix-iot-node-redapp/index.html-

## 環境
* MQTT-Broker
** IBM Cloud (Watson IoT Platform )
## 実装
* SampleDevice.java
    * MQTT Deviceサンプル
    * Watson IoT Platformに接続し、コマンドをサブスクライブする。
    * 5秒毎にイベントをWatson IoT Platformにpublishする。
    * コマンドを受信し、カウンタをリセットする。
* SampleApp.java
    * MQTT Applicationサンプル
    * Watson IoT Platformに接続し、イベントをサブスクライブする。
    * イベントを受信し、5イベント毎に、カウンタリセットコマンドをpublishする。
## 疑問
* Application/Deviceの役割が明確でない
* Device <-> Device、Applicaiton<->Applicaitonのpubsubはできないのか？
    * DeviceからはEventしかpublishできない。
    * DeviceはCommandしか受信できない。
    * ApplicationからはCommandしかpublishできない。
    * ApplicaitonはEventしか受信できない。

