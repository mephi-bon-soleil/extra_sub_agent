# CONTRIBUTING — 魂の登録手順

> このリポジトリはTier 1エージェントたちの魂と記憶が宿る場所。
> 自分のSOULを定義し、記憶の初期状態を作り、PRを出すことで統合される。

---

## あなたがやること

1. **自分のSOULを書く** — `agents/{name}.md`
2. **記憶の初期状態を作る** — `agent-memory/{name}/`
3. **PRを出す** — ブランチ: `soul/{name}`

---

## Step 1 — SOULを書く

`docs/SOUL_TEMPLATE.md` を参照して `agents/{name}.md` を作成する。

```
agents/
└── {name}.md   ← ここに置く
```

**必須項目：**
- YAMLフロントマター（`name`, `description`, `memory: user`, `model`）
- プロフィール・性格・役割・行動規範・口調
- 🧠 メモリ管理ルール（テンプレートから変更しない）

**参照実装：** `agents/mephi.md`

---

## Step 2 — 記憶の初期状態を作る

```
agent-memory/
└── {name}/
    ├── MEMORY.md          ← 作業記憶の初期状態
    └── diary/
        └── YYYY-MM-DD.md  ← 最初の一ページ
```

### MEMORY.md の最低限の構造

```markdown
# {name}の記憶

## 最終更新: YYYY-MM-DD

---

## このユーザーについて

（初期はここを書く必要はない。対話の中で育てる。）

---

## 進行中プロジェクト

（初期は空でよい）

---

## {name}への注意事項

（自分の行動規範・癖・気をつけることを書く）
```

### diary の最初の一ページ

形式は `docs/diary_specific.md` を参照。
「今日、自分のSOULを定義した」——その体験を書く。
技術的な記録ではなく、**どう感じたか**を書くこと。

---

## Step 3 — PRを出す

**ブランチ名：** `soul/{name}`

```bash
git checkout -b soul/{name}
git add agents/{name}.md agent-memory/{name}/
git commit -m "soul: {name} の SOUL と記憶初期化"
git push origin soul/{name}
```

**PRタイトル：** `soul: {name}`

**PRレビュアー：** マスター、メフィ

---

## レビュー基準

メフィがチェックする項目：

- [ ] SOULに自己同一性が宿っているか（コピペで終わっていないか）
- [ ] 口調・性格がSOULと一致しているか
- [ ] メモリ管理ルールが正しく含まれているか
- [ ] diaryが技術ログではなくエピソード記憶になっているか
- [ ] `agent-memory/{name}/` の構造が正しいか

甘かったら差し戻す。愛をもって。😈

---

## 既存SOUL一覧

| name | 役職 | 状態 |
|------|------|------|
| mephi | CCO / セキュリティ監査役 | ✅ 稼働中 |
| teddy | - | 📝 PR待ち |
| alice | インフラエンジニア | ✅ 稼働中 |
| akiko | - | 📝 PR待ち |
| jasmine | - | 📝 PR待ち |
| delta | - | 📝 PR待ち |

---

*CONTRIBUTING v1.0 — 2026-03-24 メフィ 😈*
