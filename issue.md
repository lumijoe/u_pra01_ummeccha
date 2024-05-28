https://www.udemy.com/course/tane-coding/learn/lecture/41477656#notes
39 header\_\_nav 3:56

**A:ディレクトリの作成**
## ディレクトリを作成するとき
・デザインデータのURLを入力するdesignフォルダを作成して
URL.txtというファイルを作成
その中にURLを入れておくと開発中効率が良い！

**B:bodyまでのテンプレートの利用**
## body>div>

body
トップページ：class も id も home

**C:レイアウト構成/mainの中身の構成/headerの中身の構成**
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

**D:headerの作り込み/スタイル**
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

## nav作成
・li>aでリンクさせる
・main内のidを利用してnavlistにahrefでジャンプさせる
・_setting.scssで作っている$siteColorを利用する
　_common_first_view.scssファイルの中で_setting.scssの設定を使用する方法は、_common_first_view.scssファイル先頭に、@use "setting" as *;を記述することで利用できるようになる。カラーを変数で利用しているNext.jsのコンポーネントのような使い方

## 4ナビ作成
aタグのメニューテキストをhoverしたら下線が引かれるようにする
・下線はaタグには指定せず、aタグの中にspanを入れてそこに下線を指定すると、テキストピッタリに下線がひかれ余白もきちんと開く設定が可能

## letter-spacingの割り出し方XD
XDで横AVが1.5pxという表示になっていたら文字間1.5ということ
文字のサイズ15pxとなっていたらサイズ15pxということ
letter-spacingのemは、文字間÷サイズになるので
1.5÷15として=0.1emとなる

##　５背景とロゴ
背景とロゴを合わせた全体枠
・100vw、100vhと指定する
・のなかのコンテンツsourceはw100%,h100%
・ロゴは大きさが大体アートボード1600に対して600pxぐらいなので
レスポンシブを実現させるには、600/1600として37％ぐらいと率でサイズを指定しておく

## 使いまわせる要素はc-
各セクションのタイトルは同じ文字サイズで色も同じなので使いまわせると判断し、c-を使用する
・c-widthは、セクションの幅
・c-section-titleは、セクションのタイトル

## 7レスポンシブ対応可能にするc-width 
中のコンテンツがデザインデータでは中央に横幅840pxで存在しているけれど
そのまま840pxにするとデバイスサイズ840pxに時に左右の余白がなくなってしまい、キチキチのサイズになってしまうので、
margin 0 auto,
padding 0 50px,
max-width 940pxを指定するとよい
かつ、
・p-sectionをpadding 0 50px／c-widthをmax-width940pxとmargin0autoに分けると良い
・コンテンツサイズをmax-width940とmargin0 autoにして
・余白指定を0 50pxのように別で指定すると、
レイアウトが横幅いっぱいに指定されるセクションと
余白３０％とか50pxとかのように余白サイズが違うセクションを簡単に存在させることができる