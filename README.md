# MeshiTime（メシタイム）

空き時間に行きたいお店を手軽に予約できる、飲食店予約アプリです。ユーザーはマップから近くの空いているお店を検索して予約でき、店舗側はピークタイム以外の空いている時間に空き情報を共有して、お客さんを募集できます。

専門学校3年次の授業「ITプロジェクト開発」で、5人のチームで開発しました（2026年4月〜7月）。このリポジトリは、チームのリポジトリ [RanyAS/Passione-frontend](https://github.com/RanyAS/Passione-frontend) を、コミット履歴ごと自分のアカウントにコピーしたものです。

## 主な機能

- **マップ表示**：Google Maps を使って、近くの店舗をピンで表示します。
- **店舗検索**：条件で絞り込んで、まだ行ったことのないお店を探せます。
- **予約**：ユーザーが予約すると店舗側のダッシュボードに通知が届き、店舗が予約を確認します。
- **空き情報の登録（店舗側）**：店舗が地図上にピンを立て、人数や募集時間などを入力します。入力した内容はデータベースに保存され、ユーザー側の地図に表示されます。
- **お気に入り・レビュー・来店履歴**
- **ログイン・新規登録・オンボーディング**

## 使用技術

| 分類 | 技術 |
| --- | --- |
| フロントエンド | React Native（Expo / Expo Router）、TypeScript |
| バックエンドAPI | Node.js |
| データベース | Supabase |
| 外部API | Google Maps |
| 開発環境 | Visual Studio Code |

## 自分の担当

チームではフロントエンドを担当し、主に次の作業を行いました。

- ログイン画面の作成（`meshitime/src/app/login.tsx`、`meshitime/src/styles/login.styles.ts`）
- オンボーディング画面の作成（`meshitime/src/app/onboarding.tsx`、`meshitime/src/styles/onboarding.styles.ts`）
- 新規登録画面の初期版の作成
- メンバーのブランチとのマージ作業と、コンフリクトの解消

## ディレクトリ構成

```
Meshitime/
├── .01_企画ドキュメント/   # 企画書・設計書・画面フロー図・発表資料など
└── meshitime/              # アプリ本体（Expo）
    └── src/
        ├── app/            # 各画面（Expo Router）
        ├── api/            # バックエンドAPIとの通信
        ├── components/     # 共通コンポーネント
        ├── lib/            # Supabaseの設定
        └── styles/         # 画面ごとのスタイル
```

## 実行方法

```bash
cd meshitime
npm install
npx expo start
```

※ 予約や検索などの機能を使うには、チームのバックエンドAPIとSupabaseが動作している必要があります。
