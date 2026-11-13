# Webサイトの内容更新ガイド

2026-09-15にAGENTS.mdから内容更新の説明を移管。対象はrepo rootの`index.html`。以下の例は編集時の現行HTMLに合わせ、掲載URL・repositoryはREADMEとGit設定から確認する。

## サイト構造（index.html 内のセクション）

| セクション | HTML id | 内容 |
|-----------|---------|------|
| ヘッダー | `header` | ナビゲーション（Faculty / Research / Publications / News / Access） |
| ヒーロー | （classベース） | 研究室名、所属、概要文、キーワードタグ |
| 教員紹介 | `#faculty` | 秦涼太先生のプロフィール、リンク集 |
| 研究テーマ | `#research` | カード形式で研究テーマを表示（現在3テーマ） |
| 業績 | `#publications` | 論文リスト（年降順） |
| お知らせ | `#news` | ニュース・活動報告（日付降順） |
| アクセス | `#access` | 連絡先、SNSリンク、地図 |
| フッター | `footer` | コピーライト、クレジット |

## 更新ルール

### 業績（Publications）の追加

- **挿入位置**: `<ul class="pub-list">` 内の **先頭** に追加（新しい順）
- **フォーマット**:
```html
<li class="pub-item">
  <span class="pub-year">2026</span>
  <div>
    <p class="pub-title">論文タイトル</p>
    <p class="pub-authors">著者1, 著者2, 著者3</p>
    <p class="pub-venue">ジャーナル名, Vol. XX, No. X, pp. XX–XX, 年</p>
  </div>
</li>
```
- 著者名は英語論文の場合はイニシャル形式（R. Shin）、日本語論文の場合はフルネーム（秦涼太）
- researchmap（https://researchmap.jp/RyotaShin）を参照して情報を補完してよい

### ニュース（News）の追加

- **挿入位置**: `<ul class="news-list">` 内の **先頭** に追加（新しい順）
- **フォーマット**:
```html
<li class="news-item">
  <span class="news-date">2026.04.01</span>
  <p class="news-text">
    <span class="news-badge badge-xxxxx">カテゴリ</span>
    ニュース本文
  </p>
</li>
```
- **バッジの種類**:
  - `badge-paper` （論文採択・出版）: 黄色系
  - `badge-event` （学会発表・イベント）: 緑系
  - `badge-info`  （その他お知らせ）: 青系
- 日付フォーマット: `YYYY.MM.DD`
- リンクがある場合: `<a href="URL" target="_blank" rel="noopener">テキスト</a>`

### 研究テーマ（Research）の追加・編集

- **カードフォーマット**:
```html
<div class="research-card">
  <p class="card-number">THEME 0X</p>
  <h3>テーマ名</h3>
  <p>説明文（2〜3文程度）</p>
  <div class="card-tags">
    <span class="card-tag">キーワード</span>
  </div>
</div>
```
- THEME 番号は連番で振る
- タグは3つ程度が目安

### 教員情報の変更

- `#faculty` セクション内の `.faculty-card` を編集
- 所属・職位・メールアドレスなどの変更があれば該当箇所を更新

## 参照リンク

- researchmap: https://researchmap.jp/RyotaShin
- Google Scholar: https://scholar.google.com/citations?user=Cr0DeoUAAAAJ&hl=ja
- ORCID: https://orcid.org/0000-0002-5502-9025
- X (Twitter): https://x.com/shin_frog
- Facebook: https://www.facebook.com/shin.ryota.3
