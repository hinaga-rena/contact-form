
📝 お問い合わせフォーム

📌 概要
	- 一般ユーザー向け
  - 入力フォーム（バリデーションあり）
  - 確認画面・完了画面の表示

- 管理画面
  - ログイン / ログアウト機能
  - お問い合わせ一覧表示（7件ずつページネーション）
  - 検索・絞り込み（名前、性別、カテゴリー、日付など）
  - モーダル詳細表示・削除
  - CSV出力（検索条件に応じた絞り込み）
    
 ⚙️ 環境構築手順

🐳 Dockerでビルド・起動
git clone <このリポジトリURL>
cd fashionable-late
docker-compose up -d --build

🌱 Laravel初期設定（コンテナ内で）
docker-compose exec php bash
composer create-project "laravel/laravel=8.*" . --prefer-dist
ls
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan db:seed
exit

💻 使用技術
	•	PHP: 8.x
	•	Laravel: 8.x
	•	MySQL: 8.0.26
	•	phpMyAdmin: 利用可（:8080）
	•	Nginx: 1.21.1
	•	Fortify: Laravel公式認証パッケージ

 🌐 URL
	•	開発環境 : http://localhost/
	•	phpMyAdmin : http://localhost:8080

 🖥️ アクセスURL一覧
 ユーザー登録ページ  http://localhost/registe
 ログインページ     http://localhost/login
 お問い合わせ入力　　http://localhost/
 お問い合わせ確認　　http://localhost/confirm
 お問い合わせ完了　　http://localhost/thanks
 管理画面          http://localhost/admin

## ER図
![ER図](docs/images/er.png)
 
