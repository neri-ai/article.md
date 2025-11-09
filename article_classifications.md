# テーブル設計書：タグ・カテゴリ（article_classifications）

## 1. 概要

### 1.1. テーブル名  
* article_classifications

### 1.2. 用途
* タグ・カテゴリなどの記事分類情報をまとめて管理する。

### 1.3. 改版履歴
| 日付 | バージョン | 対応者 | 対応内容 |
|------|-------|------|-------|
| 2025/11/09 | 1.0 | 根來龍志 | 新規作成 |

---

## 2. テーブル構成
| 項目 | 内容 |
|------|------|
| テーブル名 | article_classifications |
| 主キー | classification_id |
| キャラクタセット | utf8mb4 |

---

## 3. カラム仕様

| カラム名 | データ型 | NULL 許可 | デフォルト値 | 備考 |
|--------|-------|----------|--------|--------|
| classification_id | VARCHAR(6) | No | - | 分類ID |
| name | VARCHAR(100) | No | - | 分類名（タグ・カテゴリ） |
| type | ENUM('tag', 'category') | No | - | 種別 |
| created_at | DATETIME | No | - | 登録日時 |