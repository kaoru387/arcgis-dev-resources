# Web マップの作成

ArcGIS for Developers で提供される API/SDK を使って地図を作成する場合、以下の 2 つの方法に分かれます。

* __Web マップを利用する方法__
* __Web マップを利用しない方法__

ArcGIS for Developers を利用した開発では、いずれの方法でも地図アプリを作成することができますが、Web マップを利用することで地図にかかる開発コストを大幅に削減することができます。

Web マップとは背景地図や主題となる地図データを追加し、表示方法などを設定してクラウド上に保存した Web 上の地図です。Web マップの作成には ArcGIS クラウド サービスが提供する地図作成ツール（[マップ ビューアー](http://www.arcgis.com/home/webmap/viewer.html?useExisting=1)）を使用します。クラウド上に保存された Web マップを使えば、地図上に何をどのように表示するかを一つ一つコーディングする必要がなく、非常にローコストで地図アプリを作成することができます。

## Web マップの作成

### 1. Web マップの作成とレイヤーの追加

マップ ビューアーで Web マップを作成していきましょう。

<img src="http://apps.esrij.com/arcgis-dev/guide/img/webmap/addlayer.gif" width="600px">

1. [マップ ビューアー](http://www.arcgis.com/home/webmap/viewer.html?useExisting=1)を開きます。

1. 開発者アカウントでサインインします（サインインをしないと地図作成機能を利用できません）。

1. インターネットで公開されている ArcGIS クラウド サービスで共有中のレイヤーを追加します。[追加] をクリック後、[レイヤーの検索] を選択します。

1. レイヤーの検索を行います。検索先を「ArcGIS Online」とし、検索フォームにお好きなキーワードを入力して検索してみましょう。

1. 検索結果が表示されたら、追加したいレイヤーの [追加] リンクをクリックして、[レイヤーの追加を完了] ボタンを押してレイヤーの追加は完了です。
> 画像はトイレ調査と南海トラフ巨大地震の被害想定（震度/最大クラス）のレイヤーを追加しています。

### 2. レイヤーの表示方法の設定

<img src="http://apps.esrij.com/arcgis-dev/guide/img/webmap/styling.gif" width="600px">

1. レイヤーの表示設定を変えてみましょう。レイヤー リストから表現を変更したいレイヤーを選び、[スタイルの変更] アイコンをクリックします。なお、レイヤーの種類によって設定できる項目が異なります。
> レイヤーの種類はいくつかありますが、ArcGIS のクラウド サービスで配信する主なレイヤーは以下の 2 つです。フィーチャ レイヤーは Web ブラウザー上のグラフィックとして描画されるためスタイルの変更が可能です。
> * タイル レイヤー：データを画像で配信
> * フィーチャ レイヤー：データを文字列（位置座標と属性）で配信

1. [表示する属性を選択] で表示に利用する属性情報を選択し、それに応じた描画スタイルを [描画スタイルの選択] から選択します。
> 表示する属性のタイプに応じて選択できる描画スタイルは自動的に変更されます。

1. 個別値シンボルの場合は、属性値ごとに表示したいシンボルを設定することができます。シンボルを設定してみましょう。

1. レイヤー リスト上の透過率を設定したいレイヤー下にある [...] アイコンをクリックして、メニューから [透過表示] にカーソルを合わせると、スライダ－で透過率を設定できます。
> これで背景地図が見えるので場所の特定はできるようになりましたが、地震の被害想定は見たい人だけに見てほしい。そんな場合には、初期状態で非表示にしておくことができます。
> <img src="http://apps.esrij.com/arcgis-dev/guide/img/webmap/display.gif" width="450px">

1. 非表示にしたいレイヤー左にあるチェックボックスの✔を外すと、レイヤーは非表示になります。

### 3. Web マップの保存

<img src="http://apps.esrij.com/arcgis-dev/guide/img/webmap/save.gif" width="600px">

最後にここまで設定を行ってきた Web マップの保存を行います。保存すると Web マップには ID が割り当てられます。開発の際に、この ID を参照することで、設定を行った状態の地図をそのまま表示することができます。

1. [保存] ボタンをクリックし、マップの情報を入力します。入力し終わったら、[マップの保存] ボタンをクリックして、保存は完了です。
> タイトル、タグの入力は必須項目です。

1. 保存が完了すると、URL が自動的に変更されます。URL 末尾の `?webmap=<Web マップ ID>` が Web マップの ID です。メモしておきましょう。
> <img src="http://apps.esrij.com/arcgis-dev/guide/img/webmap/webmapid.png" width="600px">

---

[:back: メインページへ戻る](https://github.com/EsriJapan/arcgis-dev-resources/blob/gh-pages/README.md)