# CLAUDE.md

このファイルは Claude Code がこのリポジトリで作業する際に従うべきルールを定義する。

## プロジェクト概要

「マッチしたのは、誰？」というシナリオゲームを HTML / CSS / JavaScript で開発する。
詳細仕様は [`docs/scenario-game-spec.md`](./docs/scenario-game-spec.md) を参照。

## 技術スタック

- HTML
- CSS
- JavaScript
- 単一の `index.html` で動作することを想定

## 開発フロー（必須）

すべての開発は以下のフローに従って行う。例外なし。

1. **Issue 作成**
   開発内容は必ず先に GitHub Issue を作成する。
   Issue には背景・やること・完了条件を記載する。

2. **ブランチ作成**
   `main` から feature ブランチを切る。
   命名規則: `claude/<short-description>-issue-<番号>`
   例: `claude/add-chat-ui-issue-3`

3. **実装・コミット**
   ブランチ上で実装し、こまめにコミットする。
   コミットメッセージは Conventional Commits に準ずる:
   - `feat:` 新機能
   - `fix:` バグ修正
   - `docs:` ドキュメント
   - `refactor:` リファクタリング
   - `chore:` その他

4. **Pull Request 作成**
   `main` に向けて PR を作成する。
   PR 本文には対応する Issue 番号（`Closes #N`）を記載する。

5. **セルフレビュー**
   PR 作成後、Claude 自身がコードレビューを行い approve する。

6. **マージ**
   セルフレビュー approve 後、`main` にマージする。
   マージ方式は `squash` を基本とする。

## ブランチルール

- `main` は常にデプロイ可能な状態を保つ
- `main` への直接 push は禁止（必ず PR 経由）
- マージ済みの feature ブランチは削除して良い

## ディレクトリ構成

```
.
├── CLAUDE.md              # 本ファイル
├── README.md              # プロジェクト説明
├── index.html             # ゲーム本体（単体動作）
└── docs/                  # 仕様書類
    └── scenario-game-spec.md
```

## 参考

- 仕様書: `docs/scenario-game-spec.md`
- リポジトリ: `hirokaz/whos-matching`
