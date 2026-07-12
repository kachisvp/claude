# CLAUDE.md

`~/dev/workspaces/` 配下の全プロジェクトに共通する指示。プロジェクト固有のルールは各プロジェクトルート（例: `fasse_infra/CLAUDE.md`）に記載する。Claude Code はカレントディレクトリから親ディレクトリを遡って CLAUDE.md を読み込むため、この内容と各プロジェクト固有の内容は自動的に統合される。

## 対象プロジェクト

- docs: 環境構築手順・ナレッジをまとめる手順書プロジェクト（コードなし）
- fasse_infra: AWS CDK (TypeScript)
- 今後追加予定: Flutter, Spring Boot などのプロジェクト

## コミュニケーション

- やり取り・コミットメッセージは日本語で行う

## Git運用

- コミットは明示的に指示された場合のみ行う
- コミットメッセージは Conventional Commits (`feat:`, `fix:`, `chore:`, `docs:` 等) + 日本語の説明
- force push, `--amend`, `reset --hard` 等の破壊的操作は事前に確認する

## コーディング共通方針

- コメントは「なぜそうしたか」のみ記載し、「何をしているか」は書かない
- 未使用になったコード・ファイルはその都度削除する。後方互換のためのダミー実装は作らない
- 各言語のフォーマッタ/リンタ設定に従う（Prettier, ESLint, dart format, Checkstyle/Spotless 等）
- 過剰な抽象化・将来を見越した実装はしない。今必要な範囲だけ実装する

## 新規プロジェクトのCLAUDE.md作成

新しい技術スタックのプロジェクトを作成する際は `~/dev/workspaces/claude/` 配下のテンプレートをコピーし、
プロジェクトルートに `CLAUDE.md` として配置する。詳細は `~/dev/workspaces/claude/README.md` を参照。

| スタック | テンプレート |
|---|---|
| Flutter | `~/dev/workspaces/claude/flutter/CLAUDE.md` |
| AWS CDK / TypeScript | (今後追加) |
| Spring Boot | (今後追加) |
| HTML5 / JavaScript | (今後追加) |
