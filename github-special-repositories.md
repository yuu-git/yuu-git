# GitHub スペシャルリポジトリまとめ

GitHub には、特定の名前・配置・用途を持つことで通常とは異なる振る舞いをする「スペシャルリポジトリ」が存在する。
本ドキュメントでは、公式仕様として定義されているものと、実務上「特別扱い」されるものを整理する。

---

## 一覧まとめ

- {username}/{username} : ユーザープロフィール README
- {org}/.github : Organization プロフィール
- .github : Actions / Templates / CODEOWNERS
- 任意 + Pages : Web サイト公開
- README.md : 自動レンダリング

---

## 1. ユーザー プロフィール用リポジトリ

### {username}/{username}

例:

```
yuu-git/yuu-git
```

### 特徴
- README.md が GitHub プロフィールページの最上部に表示される
- Markdown / Mermaid / GIF / shields.io / GitHub Actions 連携が可能
- GitHub が公式に認めている唯一のユーザー単位スペシャルリポジトリ

### 主な用途
- 自己紹介
- 技術スタック・方針
- 活動ログ・バッジ
- ポートフォリオ導線

---

## 2. Organization プロフィール用リポジトリ

### {org}/.github

構成:

```
.github/
└─ profile/
   └─ README.md
```

### 特徴
- profile/README.md が Organization トップページに表示される
- チーム・OSS 向けの公式プロフィール
- 個人プロフィール README の組織版

---

## 3. .github リポジトリ（横断設定リポジトリ）

### リポジトリ名

```
.github
```

### 概要
Organization / User 配下に置くことで、複数リポジトリに共通する GitHub 設定を集約できる。

### 主な機能
- GitHub Actions テンプレート
- Issue / Pull Request テンプレート
- CODEOWNERS
- Security Policy

---

## 4. GitHub Pages 用リポジトリ

### 特徴
- 静的サイトを GitHub 上でホスティング
- Docusaurus / Jekyll / MkDocs と高相性
- ドキュメント駆動開発に向く

---

## 5. README.md が特別扱いされる場所

- リポジトリ直下 README.md → リポジトリトップに表示
- .github/profile/README.md → Organization トップに表示
- {username}/{username} → ユーザープロフィールに表示

---

## 6. 名前だけでは特別にならない例

- wiki
- website
- homepage

---
