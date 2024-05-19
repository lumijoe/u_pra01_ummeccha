## body>div>

body
トップページ：class も id も home

## 1 大きな構成：　 5 つ class/id

header,main,footer,スマホメニュー,ハンバーガーボタン

1 header l-hd header
2 main l-main main_area
3 footer l-ft footer
4 div l-sp-menu sp_menu
5 div l-sp-menu-btn sp_menu_btn

## 2 main の構成：　 5 つ class/id

first ビュー、メッセージ、オーナーや人、店舗情報、予約情報

1 header l-hd header
2 main l-main main_area
///2-1 l-home-firstview firstview
///2-2 l-section message
///2-3 l-section owner-person
///2-4 l-section shop-info
///2-5 l-section reserve-info  
3 footer l-ft footer
4 div l-sp-menu sp_menu
5 div l-sp-menu-btn sp_menu_btn

## 3 header の構成　：2 つ　

ロゴ、ナビゲーション
( \_ \_ は続けると md ではエラーが出るので半角スペースで処理している)

1 header l-hd header
///1-1 p-hd
/// 1-1-1 p-hd\_ _logo
/// 1-1-2 p-hd_ \_nav header_nav
2 main l-main main_area
///2-1 l-home-firstview firstview
///2-2 l-section message
///2-3 l-section owner-person
///2-4 l-section shop-info
///2-5 l-section reserve-info  
3 footer l-ft footer
4 div l-sp-menu sp_menu
5 div l-sp-menu-btn sp_menu_btn

## 3-a 画像 firstview の設定は picture タグで

767 以下スマホの時、768 以上パソコンの時、どちらにも合わない時などが設定できる

## 3-b ページ内リンク設定　　 home へ

ジャンプ：ページ内の異なる箇所へ移動
遷移：異なるページへ移動

## 3-c スタイル設置　

これはうまくいかなかったので next で処理した
・sass フォルダをルート直下に作成
・その中に\_common_first_view.scss ファイルを作成
・root/sass/\_common_first_view.scss を作成しコードを記述
・sass ファイルに css を記述したら,watch sass をクリックして watching にしてコンパイルする
next
・css フォルダの中に\_common_first_view.scss ファイルを作成、コードを書いてコンパイル
・Generated:
/Users/lumi/Desktop/u_pra01_ummeccha/css/home_first_view.css.map
/Users/lumi/Desktop/u_pra01_ummeccha/css/home_first_view.css 出来上がった
