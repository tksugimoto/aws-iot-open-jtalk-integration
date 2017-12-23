# aws-iot-open-jtalk-integration
AWS IoT のトピックに流れてきたメッセージを [Open JTalk](http://open-jtalk.sourceforge.net/) で再生する

## 準備
* AWS IoT の 「モノ」 を作成
    * HTTPS Rest API用 `Endpoint` をメモ
* AWS IoTにアクセス権のあるIAM ユーザーを作成
    * アクセスキーを発行し、 `Access key` & `Secret Key` をメモ
* Open JTalk Web API の作成
    * [u6k/open_jtalk-docker](https://github.com/u6k/open_jtalk-docker "https://github.com/u6k/open_jtalk-docker") を使用
        * Amazon EC2上に構築するなら [tksugimoto/terraform-amazon-ec2-open-jtalk-api](https://github.com/tksugimoto/terraform-amazon-ec2-open-jtalk-api) で自動作成可能
    * `URL` をメモ
        * クエリパラメータ（例: `?text=こんにちは` ）は含まない
        * 例: `http://localhost:8080/voice`
