# Agentic Coding Sandbox

このプロジェクトは、LLM（大規模言語モデル）を使用したエージェンティックコーディング技術を探索・開発するためのサンドボックスです。特に、cline、GitHub Copilot、Claudeなどのツールを活用したAI支援コーディングに焦点を当てています。

## 目的

- コード生成や修正のための様々なプロンプト技術を実験する
- LLM支援コーディングワークフローのベストプラクティスを開発する
- 人間とAIの効果的なコラボレーションのためのルールやガイドラインをテストし改良する
- 一般的なコーディングタスクのための再利用可能なテンプレートやパターンを作成する

## プロジェクト構造

- `.clinerules`: clineツールのコードスタイル設定
- `.github/`: GitHub設定ファイル
  - `/.github/prompts/`: 様々なコーディングタスク用の効果的なプロンプトを含む
  - `/.github/copilot-instructions.md`: GitHub Copilotのカスタム指示
- `CLAUDE.md`: Claudeとの連携に関するガイドラインとベストプラクティス

## ガイドライン

### プロンプト作成

プロンプトファイルは、Markdownファイルで完全なプロンプトを作成し、チャットで参照できるようにします。プロンプトファイルは、一般的なタスクの再利用可能なテンプレートを作成し、ドメイン知識をコードベースに保存し、チーム全体でAIとのやり取りを標準化するのに役立ちます。

プロンプト作成の詳細なテンプレートとガイドラインは、`.github/prompts/generate-prompt.prompt.md`を参照してください。

### GitHub Copilot

GitHub Copilotは、AIを活用したペアプログラミングツールです。効果的な使用方法については、以下のリソースを参照してください：

- [Copilot Chatのプロンプトエンジニアリング](https://docs.github.com/ja/copilot/using-github-copilot/copilot-chat/prompt-engineering-for-copilot-chat)
- [リポジトリカスタム指示の追加](https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot)

このプロジェクトのCopilot設定は`.github/copilot-instructions.md`で定義されています。
プロンプトは`.github/prompts/*.prompt.md`というパスで保存してください。

### Claude

Claudeとの効果的な連携のためのガイドラインとベストプラクティスは`CLAUDE.md`に記載されています。主な内容：

- Gitワークフロー
- ドキュメンテーションのメンテナンス
- ビルドと開発コマンド
- コードスタイルガイドライン
- プロジェクト構成

## コードスタイル

このプロジェクトのコードスタイル設定は`.clinerules`ファイルで定義されています。主な設定：

- 基本設定（インデント、改行、文字コードなど）
- 言語固有の設定（JavaScript/TypeScript、Python、Markdown、JSON、YAML、HTML/CSS）
- ファイル構成ルール
- コメントルール
- インポートルール

## 貢献方法

このプロジェクトへの貢献を歓迎します。貢献する際は、以下のガイドラインに従ってください：

1. プロジェクトの目的と構造を理解する
2. 適切なコードスタイルとガイドラインに従う
3. 効果的なプロンプトとAI連携のベストプラクティスを実践する
4. ドキュメントを更新し、知見を共有する

