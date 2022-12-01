# はじめに
今回自分のサーバーで試行錯誤を繰り返してきたチーム分けbotを公開botにしたいと思って、どのサーバーでも使えるように機能を更新したのでその概要を紹介していければと思います。コマンドにある[]のカッコは説明のためにつけているだけなので使うときは外してください。不具合等の報告はpinnsann@protonmail.comかtwitter([@pinnjs](https://twitter.com/pinnjs))までお願いします。
bot追加URL:https://discord.com/api/oauth2/authorize?client_id=605246939151335435&permissions=16779264&scope=bot
# コマンド一覧
## ;register
一番初めにVCのIDを設定するコマンド。<br>
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697761/dbc61ccf-66b4-2caf-d89c-eb616dad2c3e.png)<br>
上の画像のようにVCを右クリックしたら出るメニューからIDをコピーし<br>
```
;register [team1のVCID]　[team2のVCID]　[ロビー（集合場所）のVCID]
```
のように入力してください。<br>
間違えた場合はもう1回コマンドを打ち直すと更新されます。<br>
## ;td
チーム分けコマンド<br>
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/697761/651f476e-ceef-69c4-3453-97d70bbfb0d6.png)<br>
上の画像のようにキュー番号とチーム分け結果が表示されます。もちろんbotははじきます<br>
```
;td 
```
のように入力してください。<br>
後述する、勝利数タイプを下のように設定することで勝利数を加味したチーム分けになります
```
;td [勝利数タイプ]
```
## ;tdm
;tdコマンドで得たチーム分け結果を利用して、メンバーをそれぞれのVCに移動させます。キュー番号に対応させて移動させられるのでチーム分けを何回か試し一番いいものチームで移動させることも可能です。
```
;tdm [キュー番号]
```
のように入力してください。

## ;return
試合等が終わり再集合するときに使います。
```
;return
```
のように入力してください

## ;rand
マップなどを選びたいときにつかいます。１から指定数までのランダムな整数が出力されます。
```
;rand [数字]
```
のように入力してください。

## ;setwin
自分の勝利数を設定します。コマンドを打った人の勝数が変わるのでかならず自分自身でコマンドを打ってください。勝利数タイプはゲーム名やキーワードなど勝利数を紐づけるワードを選択してください。今ある数字に追加したいときはadd、今ある数字を変えたいときはreplaceを選択してください。
```
;setwin [勝利数タイプ] [add or replace] [数字]
```
のように入力してください。
## ;getwin
自分の勝利数を確認します
```
;getwin [勝利数タイプ]
```
のように入力してください。
