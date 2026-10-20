# practice-github

GitHub のアカウント作成から、ブランチ・Pull Request・レビュー・マージまでを練習するための公開サイトです。

## 公開ページ

- 練習サイト: <https://que-dotcom.github.io/practice-github/>
- 手順ガイド: <https://que-dotcom.github.io/practice-github/guide.html>

上記の URL は、リポジトリの **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save** を設定すると利用できます。公開直後は反映まで少し待ってから再読み込みしてください。

## ファイル構成

```text
practice-github/
├─ index.html             練習サイトのトップページ
├─ guide.html             参加者・主催者向けの手順
├─ profile-template.html  自己紹介ページのひな形
└─ members/
   └─ README.md           参加者の作業場所
```

参加者は自分専用の `members/<GitHubユーザー名>.html` を**作業ブランチ**で追加し、PR で `main` への取り込みを提案します。各人のファイル名を分けることで、最初の演習では編集箇所の衝突を避けられます。`main` に直接 push する手順にはしていません。

## 主催者の準備

1. GitHub Pages を上記の設定で有効にし、公開ページを確認する。
2. 参加者の GitHub ユーザー名を集める。
3. **Settings → Access → Collaborators → Add people** から招待し、参加者に承諾してもらう。公開リポジトリを見ることと、編集権限を持つことは別です。
4. レビューを必須にする場合は **Settings → Branches → Add branch protection rule** で `main` に **Require a pull request before merging** と **Require approvals** を設定する。主催者の権限や画面表示に応じて GitHub の案内に従ってください。
5. 参加者に `guide.html` を共有する。

個人情報、パスワード、トークン、秘密鍵を公開リポジトリや自己紹介ページに置かないでください。

## 参考

- [GitHub Docs: アカウント作成](https://docs.github.com/en/account-and-profile/how-tos/account-management/creating-an-account-on-github)
- [GitHub Docs: 共同編集者の招待](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration/inviting-collaborators-to-a-personal-repository)
- [GitHub Docs: Pages の公開元設定](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub Docs: ブランチ保護](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule)
