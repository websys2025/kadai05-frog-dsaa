## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能  
エンドポイント:https://zipcloud.ibsnet.co.jp/api/search?zipcode=  
機能:指定された郵便番号から住所の情報を呼び出す  
* リクエストとレスポンスのフォーマット  
リクエスト:https://zipcloud.ibsnet.co.jp/api/search?zipcode={郵便番号}  
レスポンス:JSON形式で返答　以下に具体例  
{ "message": null, "results": [ { "address1": "千葉県", "address2": "佐倉市", "address3": "井野", "kana1": "ﾁﾊﾞｹﾝ", "kana2": "ｻｸﾗｼ", "kana3": "ｲﾉ", "prefcode": "12", "zipcode": "2850855" } ], "status": 200 }
### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL  
名称:robohash
参照URL:https://robohash.org/  
* エンドポイントと機能  
エンドポイント：https://robohash.org/  
機能:指定されたidに対してロボットの画像を返す
* リクエストとレスポンスのフォーマット  
リクエスト:https://robohash.org/${id}  
レスポンス:画像で返答
### Q3-3. 感想
* 今回の課題で苦労したこと  
kadai5-2にて返答の画像を、kadai5-1と同様にfetchでデータを取得しようとしたところ、画像データとfetchの相性が悪かったのかデータを取得できなかったこと
* 演習を通して理解できたこと  
講義で紹介されたFetch APIはシンプルな文字データなどのやり取りは可能であるが、画像データには不向きであること
* Web APIの利便性や課題など  
WebAPIはデータの取得が容易である事や郵便番号の検索やロボットの画像表示など多種多様なデータのやり取りができる。その一方で適切な対処を行わない限り、エンドポイントの脆弱性を狙われるなどセキュリティ上のリスクが発生する。
