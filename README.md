# ToneStylist

## サービス概要
ToneStylistは、あと1色が決まらない人に向けた
色決定のお手伝いをするツールアプリです
___
## 想定されるユーザー層
・カーテン変えるけど、何色がいいだろう
・今持ってる服に合うアウター何色にしようかな
など、あともう1色、どうやって決めようか悩んでいる人たち
___
## サービスコンセプト

インテリアを扱う店で働いている中で、よくお客様から
「どんな色のカーテンやラグがいいか」「家の家具とかとどうバランスを取ればいいか」
というお声がけを多数いただく機会が多く、その悩みを解決するアプリがあれば、というのが出発点でした。
配色考える上でさまざまな考え方がありますが、特にカーテンやソファなどのインテリアは周囲の家具の色を踏まえた上で提案することが多いです。
そこで、「残り1色を何色にしようか」という課題解決に役立つサービスを考えました。
___

## サービスの差別化点・推しポイント
アプリでなくとも、ネットで検索をすれば色が与える印象を教えてくれるサイトはたくさん出てきます。
しかしこのアプリでは周囲に使われている色をベースに、それに合う色を探して提案する、というアプローチをかけています。それが、他のサイトなどにない推しポイントになっています。
___
## 実際の利用イメージ
* 色の提案
  1. 色登録画面を開く 
  2. 残り1色を決めるため、参考にする周囲の色を登録する。
    - 登録方法は画像を登録し、その中で最も範囲の広い色を取得する。画像は最大3枚まで登録可能
  3. 作成されたカラーチャートの確認をする。
  4. どんな雰囲気にしたいかを選択する
  5. 結果をカラーチャートで表示する。
    - ユーザー登録することで結果をお気に入り登録できる。お気に入りにしたカラーチャートにはそれを利用して購入したものやコーディネートした服装などの写真を登録できる

* 配色の印象提供
  1. マイページからお気に入りカラーチャート画面を開く
  2. カラーチャートから配色の与える印象を提供する。
    - カラーチャートに登録されたカラーコードを元に、AIによる回答の自動生成を考えています

* 商品ページへのリンク作成機能
  1. 色の提案機能で提案された色を何で利用するかを入力
  2. その色味の商品をショッピングサイトへ探しに行けるリンクを作成、商品ページへ誘導

* SNSでの共有機能
  - 作成したカラーチャートを元に購入したりコーディネートした写真を共有してもらう
___
## 実装を予定している機能
### MVP
* 配色提案機能
　- 画像の色彩を抽出する機能にVision APIのIMAGE_PROPERTIESを利用予定

* ユーザー登録機能
 - ユーザー名とメールアドレスとパスワードによる登録
* ログイン/ログアウト機能
 - 通常のメールアドレスとパスワードによるログインと、Googleアカウントとの連携によるログイン機能を予定

* 商品ページへのリンク付機能
 - 楽天市場系APIを利用予定

* SNS共有機能

### その後の機能
* 配色印象提供機能
  - PaLM2 APIのText-Bisonモデルを利用予定
___
## 使用技術（選定中）
* Ruby 3.2.1
* Rails 7系
* Vision API IMAGE_PROPERTIES(画像から色の抽出に利用)
* PaLM2 API text-bisonモデル(LLMを利用した配色提案機能で利用)
* 楽天市場系API
* TailWind CSS
* PostgreSQL
___
## 画面遷移図（URL）
https://www.figma.com/file/d0SUKZ1Rn00nZIoL3RPEeC/%E7%94%BB%E9%9D%A2%E9%81%B7%E7%A7%BB%E5%9B%B3?type=design&mode=design&t=4s5W38do32cz8dK4-0

___
## ER図
https://gyazo.com/1acbb44cc50ad09f5c4233b744c223eb