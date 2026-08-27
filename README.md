# marghetta-waiting

マルゲッタ 唐人町店の待ちリスト（ウエイティング）アプリ。
[hounantei-waiting](https://github.com/hountei/hounantei-waiting) をベースに、マルゲッタ向けにデザイン・機能を再構築したもの。

## 構成
- `index.html` — お客様の受付/待ち状況画面（`?staff=1` を付けるとスタッフ管理画面）
- `version.json` — デプロイのたびに `v` を更新すると、開いたままの画面が自動リロードされる
- `games/shooter.html` — 待ち時間に遊べる「めんたいこディフェンス」（既存ファイルをそのまま同梱）
- `games/mbti.html` — 待ち時間に遊べる「マルゲッタ性格診断」（既存ファイルをそのまま同梱）

## データ保存先
宝雲亭と同じ Firebase Realtime Database（`hounantei-waiting-default-rtdb`）を、
パス `/marghetta/state` で共用している。

## デプロイ
GitHub Pages（`main` ブランチ、リポジトリ直下）を想定。
新しいバージョンを配布する際は `index.html` 内の `APP_VERSION` と `version.json` の `v` を同じ値に更新すること。
