# ポートフォリオサイト

## 目的：
* 作品を紹介し広く知ってもらう  
* 作品を作るモチベーションを高め、スキルアップにつなげる  
* (ゆくゆくは)仕事を受けるプラットフォームとして活用したい  
* 自身の取り組みを知らせるメディアとしての利用

## 環境：
* WordPress（WP）を使用可のレンタルサーバー  
* WPのローカル環境（）  
* フォーム[Googlefoam　か　contact7₍WP₎]を使用  
* SNSの使用を検討[Blue Sky、line]  

## 手順：
1. サイトの構成決定（WP組込も想定して）  
1. HTMLのみでサイト作成  
1. ローカル環境を設置してサイトをWPに組み込む:　手段検討中  
1. 組込後、問題ないかチェック  
1. レンタルサーバーに設置、ここでも問題ないかチェック  
1. サイト公開  
1. 都度、サイト修正・ブラッシュアップに取り組みつつ、作品作成→アップしていく。

## 構成：
- メインナビ
``` 
    HOME

    WORKS
    ｜→ WEB: 架空のコーポレートサイト、バナー、ロゴ　の紹介
            (term: site,bannar,logo)
    ｜→ FLIER: 広告物（チラシ・ポップ）の紹介
            (term: event,pop,service)
    ｜→ OTHER: プログラミングや他カテゴリーの作品を紹介
            (term: PG,AI)

    ABOUT  

    CONTACT

```

- 各ページ  
```
HOME(WP:home.php)
```
```
WORKS(WP:works.php カスタムテンプレート-各termのindexページとして使用)  
    ｜→ WEB(WP:taxonomy.php カスタム分類ページ)  
        ｜→ WEB(WP:single.php 個別ページ)

    ｜→ FLIER(WP:taxonomy.php カスタム分類ページ)
        ｜→ FLIER(WP:single.php 個別ページ)
        
    ｜→ OTHER(WP:taxonomy.php カスタム分類ページ)
        ｜→ OTHER(WP:single.php 個別ページ)

インクルードタグ: sidebar.php (term毎のナビゲーション設置)
※個別ページにカスタムフィールド・アイキャッチ画像設定
```
```
ABOUT(WP:page.php 固定ページ )
```
```
CONTACT(WP:page.php 固定ページ )　※contactform7　か　Googlefoam　を使用
```
```
共通のインクルードタグ: 
header.php : グローバルナビ、サイトロゴ
footer.php : コピーライト、トップページリンク
```
```
その他：
404.php
functions.php
```