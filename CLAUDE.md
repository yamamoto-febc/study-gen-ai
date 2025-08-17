# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

このプロジェクトではClaudeとのやりとりに日本語を用います。

## プロジェクト概要

「生成AI入門講座」は、中高生向けにChatGPTやGoogle Geminiを日常で「思考のパートナー」として使いこなすための教材プロジェクトです。

このリポジトリに含まれるもの：
- インタラクティブな教育プラットフォームとしてのシングルページHTMLアプリケーション
- README.md、LICENSE、LICENSE-CONTENTなどのドキュメント
- `docs/`ディレクトリ内の静的アセット

## アーキテクチャ

### 技術スタック
- **フロントエンド**: 純粋なHTML、CSS、JavaScript（ビルドツール不要）
- **スタイリング**: Tailwind CSS（CDN経由で読み込み）
- **フォント**: Google Fonts（InterとNoto Sans JP）
- **デプロイ**: GitHub Pages（https://yamamoto-febc.github.io/study-gen-ai/）

### ファイル構造
```
study-gen-ai/
├── docs/
│   ├── index.html          # メインのインタラクティブ講座アプリケーション
│   └── og_image.png        # ソーシャル共有用のOGイメージ
├── LICENSE                 # コード用MITライセンス
├── LICENSE-CONTENT         # 教育コンテンツ用CC-BY 4.0ライセンス
└── README.md              # 日本語プロジェクト説明
```

### アプリケーション設計
メインアプリケーション（`docs/index.html`）の特徴：
- **ナビゲーション**: 講座チャプター（第0回-第4回）付き折りたたみサイドバー
- **コンテンツ**: JavaScriptオブジェクトとして埋め込まれた講座内容
- **インタラクティブ要素**: コピーボタン、タブインターフェース、タイムライン
- **レスポンシブデザイン**: ハンバーガーメニュー付きモバイル対応
- **カラースキーム**: カスタム茶/ベージュテーマ（#A58A73, #D4C5B8, #FDFBF8）

## 開発コマンド

これは静的HTMLプロジェクトなので、ビルドツールやパッケージマネージャーは不要：

- **ローカル開発**: `docs/`ディレクトリを任意の静的Webサーバーでサーブ
- **テスト**: `docs/index.html`を直接ブラウザで開いて基本テスト
- **デプロイ**: mainブランチへのプッシュで自動的にGitHub Pagesデプロイ

## コンテンツ管理

### 講座構造
講座コンテンツはHTMLファイル内にJavaScriptオブジェクトとして直接格納：
- `content-0`: オリエンテーション
- `content-1`: AIを「賢い道具」に
- `content-2`: AIとの「対話」
- `content-3`: AIは「思考加速ツール」
- `content-4`: AIを「専門家チーム」に

### ライセンス
- **コード**: MITライセンス（HTML、CSS、JS）
- **コンテンツ**: CC-BY 4.0（教育テキストと画像）
- クレジット表記要件: "© 2025 yamamoto-febc, licensed under CC-BY 4.0"

## 保持すべき主要機能

アプリケーションを修正する際は以下を維持：
- 日本語教育コンテンツの保持
- モバイルデバイス向けレスポンシブデザインの維持
- インタラクティブ要素（コピーボタン、タブ、タイムライン）の機能性維持
- 適切なセマンティックHTMLによるアクセシビリティ確保
- カスタムカラースキームとタイポグラフィの保持