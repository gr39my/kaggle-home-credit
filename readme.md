# 概要
home creditのkaggle日記です

## 2024/3/23
- kaggle日記をつけ始めました
- 特徴量の和訳シートを作成
  - https://docs.google.com/spreadsheets/d/1u8F2wGdRaXsSfGjlvmMK4UhXVv-pbTqAmVBeQU_eTw0/edit#gid=0
 
## 2024/3/24
- kaggle notebookでセッション切れが多発して進捗いまいちだったので、colabの準備
- k-foldが1回でbreakできるように書き換えた
- Home Credit: Baseline using Depth0 Data___ver06をsubmit→エラーで失敗
  - lgbmClassで予測（0,1を予測）したため、lgbmで0~1を予測した方が良さそう
  - Depth0のデータまでを使った予測
- Home Credit: Baseline using Depth0 Data___ver07で再度submit
  - エラーを解消
  - colabで修正したものをkaggle notebookに反映できていない部分があった
  - 例えば「from sklearn.metrics import roc_auc_score」を追加し忘れた、ようなもの
- Home Credit 2024 Starter Notebookをメインで参考にした
  - https://www.kaggle.com/code/jetakow/home-credit-2024-starter-notebook 
- submitが無事にできたらclassではなくて普通のlgbmと比較したい。

## 2024/3/25
- 「Home Credit: 特徴量の日本語訳」をpublicで投稿しなおした
  - コンペの紐付けせずに投稿してしまっていたのを、紐づけた
  - コンペのデータセットを使用していなくても、inputに追加しておくと、そのコンペのcodeに表示されるようになるよう。

## 2024/3/26(2時間)
- 今日からkaggleに取り組んだ時間も記録することにしました。
- codeコンペの採点方法について調べた。
- 昨日、投稿しなおしたnotebookが銅メダル!!嬉しい
- 「Simplest baseline using only depth=0 data」をpublicで投稿
- これまで簡単のために depth=0 のデータのみに絞っていたので、明日からdepth=0,1,2と1つずつ増やしていく!!
