# Bitcoin Blockchain Explorer — Vercel 公開手順

## 所要時間：約10分（すべてブラウザ上で完結）

---

## ステップ 1: GitHubアカウントを作成（すでにあればスキップ）

1. https://github.com にアクセス
2. 「Sign up」をクリック
3. メールアドレス、パスワード、ユーザー名を入力して作成

---

## ステップ 2: GitHubにリポジトリを作成してファイルをアップロード

1. GitHubにログインした状態で https://github.com/new にアクセス
2. 「Repository name」に `btc-explorer` と入力
3. 「Public」を選択
4. 「Create repository」をクリック
5. 作成されたページで「uploading an existing file」のリンクをクリック
6. ダウンロードしたzipを解凍して出てきた **btc-explorerフォルダの中身すべて** をドラッグ&ドロップ
   - ⚠️ フォルダ自体ではなく、中のファイル（package.json, index.html, src/, public/ など）をアップロードしてください
7. 「Commit changes」をクリック

---

## ステップ 3: Vercelに接続してデプロイ

1. https://vercel.com にアクセス
2. 「Start Deploying」→「Continue with GitHub」でGitHubアカウントでログイン
3. 「Import Project」画面で `btc-explorer` リポジトリを選択
4. 設定画面が出たら **何も変更せずに**「Deploy」をクリック
   - Vercelが自動でVite + Reactを検出してビルドします
5. 1〜2分でデプロイ完了！🎉
6. `https://btc-explorer-xxxxx.vercel.app` のようなURLが発行されます

---

## ステップ 4: カスタムドメインの設定（任意）

1. Vercelのプロジェクトダッシュボードで「Settings」→「Domains」
2. 使いたいドメインを入力（例: `blockchain.cryptact.com`）
3. 表示されるDNSレコードをドメインのDNS設定に追加
4. 数分で反映されます

---

## 更新方法

ファイルを更新したい場合：
1. GitHubのリポジトリページを開く
2. 更新したいファイルをクリック → 鉛筆アイコンで編集、またはファイルを再アップロード
3. 「Commit changes」すると、Vercelが自動で再デプロイします

---

## トラブルシューティング

**ビルドエラーが出た場合：**
- Vercelダッシュボードの「Deployments」タブでエラーログを確認
- 大抵はファイル配置の問題（フォルダの中身ではなくフォルダ自体をアップロードした場合など）

**画面が真っ白になる場合：**
- ブラウザのキャッシュをクリアして再読み込み
- Vercelダッシュボードで「Redeploy」をクリック
