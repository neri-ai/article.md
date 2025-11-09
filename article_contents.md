# テーブル設計書：記事本文・編集履歴（article_contents）

## 1. 概要

### 1.1. テーブル名  
* article_contents

### 1.2. 用途  
* 記事本文をMarkdown形式度保持する。将来的に編集履歴(バージョン管理)を行う。

### 1.3 改版履歴  
| 日付 | バージョン | 対応者 | 対応内容 |
|------|---------|------|--------|
| 2025/11/09 | 1.0 | 根來龍志 | 新規作成 |

---

## 2. テーブル構成
| 項目 | 内容 |
|-------|-------|
| テーブル名 | article_contents |
| 主キー | contents_id |
| 複合キー | article_id |
| キャラクタセット | utf8mb4 |

---

## 3. カラム使用
| カラム名 | データ型 | NULL 許可 | デフォルト値 | 備考 |
|-------|-------|-------|-------|-------|-----|
| contents_id | VARCHAR(6) | No | - | コンテンツID |
| article_id | VARCHAR(6) | No | - | 記事ID(複合キー) |
| body | TEXT | No | - | Markdown本文 |
| version | INT | No | 0 | 編集バージョン |
| created_at | DATETIME | No | - | 作成日時 |
| updated_at | DATETIME | No | - | 更新日時 |
