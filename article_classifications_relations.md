# テーブル設計書：記事と分類の中間テーブル(artcile_classifications_relasitons)

## 1. 概要

### 1.1. テーブル名  
* article_classification_relations

### 1.2. 用途
* 記事と分類(タグ・カテゴリ)の多対多関係を管理する中間テーブル。

### 1.3. 改版履歴  
| 日付 | バージョン | 対応者 | 対応内容 |
|------|-------|------|-------|
| 2025/11/09 | 1.0 | 根來龍志 | 新規作成 |

---

## 2. テーブル構成
| 項目 | 内容 |
|------|------|
| テーブル名 | article_classification_relations |
| 主キー | article_id |
| 主キー | classification_id |
| 複合キー | article_id |
| 複合キー | classification_id |
| キャラクタセット | utf8mb4 |

---

## 3. カラム使用

| カラム名 | データ型 | NULL 許可 | デフォルト値 | 備考 |
|--------|------|-------|-------|-------|
| artcile_id | VARCHAR(6) | No | - | 記事ID |
| classication_id | VARCHAR(6) | No | - | 分類 |