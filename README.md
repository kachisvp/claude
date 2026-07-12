# claude/ ディレクトリについて

各技術スタック用の CLAUDE.md テンプレートを保管する場所。`~/dev/workspaces/` 配下に新しいプロジェクト（リポジトリ）を作成した際、該当するテンプレートをコピーしてプロジェクトルートに `CLAUDE.md` として配置する。

## 使い方

```
cp ~/dev/workspaces/claude/flutter/CLAUDE.md ~/dev/workspaces/<new_flutter_project>/CLAUDE.md
```

コピー後、プロジェクトの実態（概要・ディレクトリ構成・使用パッケージなど）に合わせて内容を編集する。

## 読み込みの仕組み

Claude Code は起動時にカレントディレクトリから親ディレクトリをルートまで遡って見つかった CLAUDE.md をすべて読み込む。そのため `~/dev/workspaces/CLAUDE.md`（共通）と `<project>/CLAUDE.md`（プロジェクト固有）の両方が自動的に読み込まれ、内容が統合される。

このディレクトリ自体はテンプレートの置き場であり、コピーしてプロジェクトルートに配置するまでは読み込み対象にならない。

## テンプレート一覧

- `flutter/CLAUDE.md`: Flutter プロジェクト用
