# はじめに
今回自分のサーバーで試行錯誤を繰り返してきたチーム分けbotを公開botにしたいと思って、どのサーバーでも使えるように機能を更新したのでその概要を紹介していければと思います。コマンドにある[]のカッコは説明のためにつけているだけなので使うときは外してください。不具合等の報告はpinnsann@protonmail.comかtwitter([@pinnjs](https://twitter.com/pinnjs))までお願いします。
bot追加URL:https://discord.com/api/oauth2/authorize?client_id=605246939151335435&permissions=16779264&scope=bot
# コマンド一覧
## ;register
一番初めにVCのIDを設定するコマンド。<br>
![image.png](https://github.com/pinnsann/team_division_discord_bot/blob/main/td%20image/register.png?raw=true)<br>
上の画像のようにVCを右クリックしたら出るメニューからIDをコピーし<br>
```
;register [team1のVCID]　[team2のVCID]　[ロビー（集合場所）のVCID]
```
のように入力してください。<br>
間違えた場合はもう1回コマンドを打ち直すと更新されます。<br>
## ;td
チーム分けコマンド<br>
![image.png](https://github.com/pinnsann/team_division_discord_bot/blob/main/td%20image/td.png?raw=true)<br>
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

## ;replacewin
勝利数を書き換えます。勝利数タイプはゲーム名やキーワードなど勝利数を紐づけるワードを選択してください。メンションがない場合コマンドを実行した本人、メンションした場合メンションした人の勝利数を書き換えます。
```
;replacewin [勝利数タイプ] [数字] [メンション]
```
のように入力してください。
## ;controlwin
勝利数を操作します。コマンドを使うと以下の画像のようなメッセージが表示されます。
![image.png](https://github.com/pinnsann/team_division_discord_bot/blob/main/td%20image/controlwin.png?raw=true)<br>
下のリアクションを押すとそれぞれのアクションがなされます。左から順番に上矢印は勝利数を一つ上げる、下矢印は一つ下げる、2つ矢印は０にする、ばつ印はこのメッセージを消去する事ができます。
```
;controlwin [勝利数タイプ] [メンション]
```
のように入力してください。
