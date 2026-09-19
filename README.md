[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526682619)

# Use GitHub Copilot to write JavaScript

Explore how you can modify a JavaScript repository using code suggestions from GitHub Copilot to modify and customize a web application. By working with this repository, you'll quickly get hands-on with a JavaScript web app for a portfolio site.

## プロジェクト概要

このプロジェクトは、GitHub Copilot を使ってカスタマイズできる React 製のポートフォリオサイトです。プロフィール、自己紹介、スキル、制作物、SNS やメールへの連絡先を 1 ページにまとめて表示します。

アプリケーションは Parcel で開発・ビルドします。サイトの基本情報や SNS アカウントは `src/App.jsx` の `siteProps` に定義され、各コンポーネントへ props として渡されます。画像や配色を変更することで、自分用のポートフォリオへ簡単に置き換えられます。

## リポジトリ構成

```text
.
├── .devcontainer/
│   └── devcontainer.json       # GitHub Codespaces の開発環境設定
├── src/
│   ├── App.jsx                 # ページ全体の構成とサイト情報
│   ├── index.html              # HTML エントリポイント
│   ├── index.js                # React アプリケーションのマウント
│   ├── styles.css              # アプリケーション共通のスタイル
│   ├── Components/
│   │   ├── Header.jsx          # 固定ナビゲーション
│   │   ├── Home.jsx            # トップのプロフィール表示
│   │   ├── About.jsx           # 自己紹介とスキル一覧
│   │   ├── Portfolio.jsx       # 制作物・プロジェクト一覧
│   │   └── Footer.jsx          # SNS とメールの連絡先
│   └── images/
│       ├── *.jpg / *.jpeg      # 各セクションの背景・表示画像
│       └── socials/            # SNS・メールのアイコン
├── translations/               # 翻訳関連の README
├── package.json                # 依存関係と npm スクリプト
├── package-lock.json           # 依存関係の固定情報
├── .eslintrc                   # ESLint 設定
├── .prettierrc                 # Prettier 設定
├── LICENSE                     # リポジトリのライセンス
├── LICENSE-CODE                # コードのライセンス
├── SECURITY.md                 # セキュリティポリシー
└── README.md                   # プロジェクト説明と学習手順
```

### 主な実行コマンド

- `npm install`: 依存パッケージをインストール
- `npm start`: 開発サーバーを起動
- `npm run build`: 本番用ファイルを `dist/` にビルド
- `npm run deploy`: GitHub Pages へデプロイ

## Requirements

1. Enable your [GitHub Copilot service](https://github.com/github-copilot/signup)
1. Open [this repository with Codespaces](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-javascript?quickstart=1)

## 💪🏽 Exercise

In this template portfolio, we have a React based web application ready for you to easily customize and deploy using only your web browser.


### 🛠 Step 1: Customize the web app

Customize the portfolio with your own links. Go to `src/App.jsx` and update the `siteProps` with your information. The `siteProps` variable is a JavaScript object that holds key value pairs used to customize the site, it should look like this:

```javascript
const siteProps = {
  name: "Alexandrie Grenier",
  title: "Web Designer & Content Creator",
  email: "alex@example.com",
  gitHub: "microsoft",
  instagram: "microsoft",
  linkedIn: "satyanadella",
  medium: "",
  twitter: "microsoft",
  youTube: "Code",
};
```

### 🔎 Step 2: Animate the social media icons with a prompt

An animation can make the social media section more eye-catching. Ask Copilot’s help to animate the icons. Write the following prompt in the `src/styles.css` file:

```css
/* add an amazing animation to the social icons */
```

The suggestion from Copilot should look similar to the following:

```css
img.socialIcon:hover {
  animation: bounce 0.5s;
  animation-iteration-count: infinite;
}

@keyframes bounce {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
```

### 🚀 Step 3: Find out how to run the app
Open GitHub Copilot chat by clicking on the chat icon on the left side bar and use the input section to ask the following:

```
@workspace I want to understand how can I run this React application
```

The prompts uses `@workspace` which is a special feature of GitHub Copilot chat that allows you to include more context for a more complete answer. Try out other queries using the chat panel for a more interactive workflow.

### Conclusion
Your site should already be running in your Codespace, and the change will reload onto the page automatically. To see them, hover over one of your social media icons in the footer to see the magic!

Congratulations, through the exercise, you have use GitHub Copilot to generate code and also done it in an interactive and fun way! You can use GitHub Copilot to not only generate code, but write documentation, test your applications and more.
