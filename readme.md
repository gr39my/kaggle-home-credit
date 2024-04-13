# 概要
home creditのkaggle日記です

# 実験記録


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

## 2024/3/28(1.5時間)
- depth=1のデータを追加
- depth=1のデータは１つのcase_idごとに複数のnum_group1が存在する。
- そのため、maxを取ったりしながら追加することになりそう

## 2024/3/29(1時間)
- ディスカッションを眺めていたら時間が溶けた
- 明日は、気になったものを動かしてみる
  - https://www.kaggle.com/code/dksdms4/lb-0-565-improved-baseline-notebook
 
## 2024/3/30(5時間)
- [[LB:0.565]Improved baseline Notebook](https://www.kaggle.com/code/dksdms4/lb-0-565-improved-baseline-notebook)を動かしてみる
- コードの解読しかできていないのでは...???
- [colabで動かす](https://colab.research.google.com/drive/1mH_RF1LvgE8gwVe4fzOrD8M6Kt_T6YHF#scrollTo=j1Bby4s7vV2N)ときにGPUがないよ！的なエラーが発生する...
  - あしたはここを解決する。
  - 訓練の部分は、いまいち上手に動かないので、自分で作成したスクリプトで埋める
 
## 2024/3/31(1時間)
- 引き続き、訓練の部分は、いまいち上手に動かないので、自分で作成したスクリプトで埋める
- 課題の言語化
  - ![image](https://github.com/gr39my/kaggle-home-credit/assets/68382023/9e17f320-556b-4758-b094-e33d24eca62c)
 
## 2024/4/2(2時間)
- 訓練部分を差し替え
- kfoldを10000にして、訓練を早くおわるようにした

## 2024/4/3~2024/4/7（毎日30分くらい）
- pandasの状態で特徴量エンジニアリングして、submitまで行った
- logを見るとエラーはないものの、スコアが計算されていないので、なにかしらのエラーがありそう。。。
- 「自分で書いたコードでsubmit+スコアもらえる」のを目標にしたい

## 2024/4/9~13（毎日1時間くらい）
- 1つエラーを修正すると、別のエラーが発生したりメモリ不足になったりと悪戦苦闘
- いろんなものをコメントアウトして最低限の状態になってしまったけれど、submitが通った。
- スコアは0.526

## 2024/4/14
- 5:30-
