# CLAUDE.md (Flutter)

Flutter プロジェクトのルートに `CLAUDE.md` としてコピーして使うテンプレート。共通ルールは `~/dev/workspaces/CLAUDE.md` を参照（自動的に統合される）。

## このプロジェクトについて

(プロジェクトの概要をここに記載)

## コマンド

```
flutter pub get
flutter analyze
flutter test
flutter run
```

## ディレクトリ構成

- feature-first: `lib/features/<feature_name>/` に UI・状態管理・モデルをまとめる
- 共通部品は `lib/shared/` に置く

## 規約

- 状態管理: Riverpod
- Widget は1ファイル1Widget、Stateless優先（必要な場合のみ StatefulWidget）
- `print()` は禁止。`logger` パッケージを使う
- l10n は ARB ファイルで管理する

## テスト

- ロジックは `test/` にユニットテストを書く
- Widget テストは `test/widgets/` に置く
- PR前に `flutter analyze` と `flutter test` を通す
