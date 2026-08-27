# Zenn コンテンツ

Zenn 個人アカウント [`@koenigwolf`](https://zenn.dev/koenigwolf) の記事・本を管理する非公開リポジトリです。

## セットアップ

```bash
npm ci
npm run preview
```

ローカルプレビューは `http://localhost:8000` で確認できます。

## 記事の作成

```bash
npm run new:article -- --slug example-article
```

作成直後は Front Matter の `published: false` を維持してください。公開を承認した記事だけ、別の変更で `published: true` にします。

## PR での確認

1. `main` から作業ブランチを作成します。
2. 記事と画像を編集し、`npm run preview` で表示を確認します。
3. `main` 向けに PR を作成します。
4. Zenn の「PR で下書きデプロイ」で下書き表示を確認します。
5. 公開する場合は、内容の確認後に `published: true` へ変更して Merge します。

PR を Close または Merge しても、Zenn にデプロイされた下書きや画像は自動削除されません。不要なデータは Zenn 側で手動削除してください。

## 安全上の注意

- 記事は `articles/`、本は `books/`、画像は `images/` に配置します。
- Secret、個人情報、顧客情報、社外秘情報を Commit／PR に含めないでください。
- Fork からの PR は、Zenn の PR 下書きデプロイ対象外です。
- Zenn Connect の GitHub 権限は、このリポジトリだけに限定します。

詳しい記法とコマンドは [Zenn CLI の使い方](https://zenn.dev/zenn/articles/zenn-cli-guide)を参照してください。
