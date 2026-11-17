SUKIMA PLAN（アプリ版）

■ フォルダの中身
  ai_project.html        アプリ本体
  index.html             ai_project.html への入口
  manifest.webmanifest   アプリ情報（名前・アイコン・色）
  sw.js                  オフライン用の仕組み（Service Worker）
  icon-*.png             アイコン

■ 注意
  アプリとしてインストールするには HTTPS で公開されたURL（または localhost）で開く必要があります。
  ファイルをダブルクリックして開く方法（file://）でも普通に使えますが、インストールとオフライン保存の仕組みは働きません。

■ パソコンで試す（localhost）
  1. このフォルダでターミナルを開く
  2. python3 -m http.server 8000
  3. Chrome で http://localhost:8000/ を開く
  4. アドレスバー右端のインストールアイコン → インストール

■ スマホにインストールする
  1. このフォルダごと、無料のホスティング（Netlify Drop / GitHub Pages / Cloudflare Pages など）にアップロード
  2. 発行された https:// のURLをスマホで開く（1回開けばオフラインでも起動できます）
  3. Android(Chrome): メニュー → 「アプリをインストール」または「ホーム画面に追加」
     iPhone(Safari): 共有ボタン → 「ホーム画面に追加」

■ 更新するとき
  ai_project.html を差し替え、sw.js の V（'sukima-plan-v1'）を v2, v3… に変えてアップロード。

■ データについて
  予定などの保存先はブラウザ内で、開くURLごとに別になります。
  ファイル版から公開URL版へ移すときは、☰メニューの「保存」→ 新しい方で「読込」を使ってください。
