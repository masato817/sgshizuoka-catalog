# Webサイトの公開方法 (GitHub Pages)

現在、カタログのHTMLファイルに写真が埋め込まれました。これをインターネット上で誰でも見られるように公開する手順をご案内します。

今回は、無料で簡単に使える **GitHub Pages** を使う方法がおすすめです。

## 手順

### 1. Gitの初期化とコミット

Cursorのターミナル（`Ctrl + @` で開けます）で以下のコマンドを順番に入力して実行してください。

```bash
# 1. Gitの初期化
git init

# 2. 全ファイルをステージング（登録準備）
git add .

# 3. コミット（保存）
git commit -m "カタログサイトの作成（写真追加）"
```

### 2. GitHubリポジトリの作成

1.  Webブラウザで [GitHub](https://github.com/) にログインします。
2.  右上の「+」アイコンから「New repository」を選択します。
3.  **Repository name** に好きな名前（例: `mossfarm-catalog`）を入力します。
4.  **Public**（公開）が選ばれていることを確認します。
5.  「Create repository」ボタンをクリックします。

### 3. GitHubへアップロード

リポジトリ作成後に表示される画面にあるコマンド（`…or push an existing repository from the command line` の部分）をコピーして、Cursorのターミナルで実行します。

例（ユーザー名などはご自身のものに置き換わります）:
```bash
git remote add origin https://github.com/あなたのユーザー名/mossfarm-catalog.git
git branch -M main
git push -u origin main
```

### 4. 公開設定

1.  GitHubのリポジトリページで、上部のタブから **Settings** をクリックします。
2.  左側のメニューから **Pages** をクリックします。
3.  **Build and deployment** の **Source** が `Deploy from a branch` になっていることを確認します。
4.  **Branch** のところを `None` から `main` に変更し、隣のフォルダは `/(root)` のまま **Save** をクリックします。

### 5. 完成！

数分待つと、ページの上部に公開されたURL（例: `https://あなたのユーザー名.github.io/mossfarm-catalog/`）が表示されます。
このURLをクリックすると、Webサイトが見られます。

---

### うまくいかない場合

もしコマンド操作が難しい場合は、**Netlify Drop** というサービスも便利です。
1.  [Netlify Drop](https://app.netlify.com/drop) にアクセスします。
2.  `カタログ` フォルダごと、ブラウザの枠内にドラッグ＆ドロップします。
3.  これだけで公開されます！
