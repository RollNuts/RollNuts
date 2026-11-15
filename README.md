# RollNuts

AIを使って、個人でソフトウェアを作っています。5年後にありそうな出来事を新聞にする[未発生新聞](https://veripsa.com)と、コードを変える前に関連ファイルを探す[Veripsa Core](https://github.com/RollNuts/veripsa)を作っています。

## AIで何かを作っていて、こんなときは

**AIに頼んだ修正、答えが合っていれば採用していい？**

小さな会計プログラムを直す二択問題です。どちらの案でも、手数料を足した合計は105。頼んだ条件まで守っているのはどちらでしょう。選んだら、その場で答えを開けます。[GitHubで二択を試す](https://github.com/RollNuts/zenn-content/tree/main/examples/api-contract-repair)

**サイトを更新したのに、古い画面が出てくる。どこを確かめる？**

公開先に小さな目印を置き、古い版が届いているのか、一部だけが入れ替わったのかを見分ける例です。[Zennで確かめ方を読む](https://zenn.dev/veripsa/articles/ci-success-deployed-revision)

**AIにファイルの修正を頼む前に、ほかのどこを一緒に読んでもらう？**

Veripsa Coreで、コードのつながりと過去に一緒に変わった履歴から、次に読むファイルの候補を出せます。[自分のリポジトリで試す](https://github.com/RollNuts/veripsa/blob/main/docs/LOCAL_FILE_REVIEW.md) · [日本語ガイド](https://github.com/RollNuts/veripsa/blob/main/docs/README.ja.md)

<details>
<summary>Veripsa Coreの実行コマンドと利用条件</summary>

新しい作業用ディレクトリで、まずCore自身を調べられます。

```sh
git clone https://github.com/RollNuts/veripsa.git
cd veripsa
python3.12 -B -m tools.review_file . _cg_cochange.py
```

自分のrepoでは、最後の2引数をGitルートと相対ファイル名へ置き換えます。POSIX環境のGit＋Python 3.12が必要で、Python入力なら追加パッケージ・DB・モデルAPI・アカウントは不要です。対象コードは実行しません。候補には誤りや欠落があり、空でも安全の証明にはなりません。出力のパス等は共有前に確認してください。

頻繁なGitコンフリクトを減らしたくて作り始めた仕組みから、コードグラフ・Co-change・永続化の技術が生まれました。[4つの合成例](https://github.com/RollNuts/veripsa/tree/main/examples/structural-overlap)では、Gitのclean merge、構造と履歴の関連、統合後の実行を比較できます。[解析基盤とDBの役割](https://github.com/RollNuts/veripsa/blob/main/docs/ANALYSIS_ASSETS.md)も公開しています。

ライセンスは[BSL 1.1 / source-available](https://github.com/RollNuts/veripsa/blob/main/LICENSE)です。ホスト型GitHub Appは停止中です。

</details>

## Main projects / 主なプロジェクト

| Project | What you can explore | Current status |
| --- | --- | --- |
| [Veripsa Core](https://github.com/RollNuts/veripsa) | Code graph, historical co-change, and durable PR coordination. [Review your own file](https://github.com/RollNuts/veripsa/blob/main/docs/LOCAL_FILE_REVIEW.md) · [Implementation inventory](https://github.com/RollNuts/veripsa/blob/main/docs/ANALYSIS_ASSETS.md) · [Pinned Flask evaluation](https://github.com/RollNuts/veripsa/blob/main/docs/OFFLINE_EXAMPLE.md). | Source-available; hosted GitHub App is suspended. |
| [Mihassei News / 未発生新聞](https://github.com/RollNuts/mihassei-news) | A fictional satire newspaper built with Python, static pages, and Cloudflare Workers. [Read it](https://veripsa.com) or build it locally. | Active project; local build needs no API credentials. |

## Agent integration / AIから使う実験

[Core → local MCP / Codex](https://github.com/RollNuts/zenn-content/tree/df6d5c739f3f6c79f14ead14e275ad3e766f5cd9/examples/core-local-mcp) — a separate read-only adapter for a saved Tauri snapshot. SDK-only reproduction is model-free; optional Codex execution uses the signed-in account's allowance. [日本語の解説（Zenn）](https://zenn.dev/veripsa/articles/tauri-command-contract-graph) · [GitHub原稿](https://github.com/RollNuts/zenn-content/blob/main/articles/tauri-command-contract-graph.md).

## Technical writing / 技術記事

[Zenn](https://zenn.dev/veripsa) — Japanese implementation, code-analysis, and operations notes on Git, Python, RSS, and static sites.

[記事の更新をRSSで購読 / Subscribe via RSS](https://zenn.dev/veripsa/feed)

- [この修正、ほかにどこを確認する？ コードのつながりとGit履歴を4例で比べた](https://zenn.dev/veripsa/articles/graph-cochange-review-benchmark) — 4つの合成例を、手元で実マージ・実行・採点する。
- [このブランチ、もう消していい？ GitHubで556本を調べて103本を残した理由](https://zenn.dev/veripsa/articles/github-branch-cleanup-squash-556)
- [5年後の新聞を今日公開する。RSSにはいつの日付を載せる？](https://zenn.dev/veripsa/articles/fiction-date-rss-static-site)
- [Article sources](https://github.com/RollNuts/zenn-content) — maintained through Zenn's GitHub integration.

## Reference repositories / 検証・参照用

- [ai-pr-collision-lab](https://github.com/RollNuts/ai-pr-collision-lab) — historical PR-collision recordings and a local pricing-test fixture. Current engine development is in Veripsa Core.
- [awesome-cli-coding-agents](https://github.com/RollNuts/awesome-cli-coding-agents) — reference fork. Current curation and submissions belong [upstream](https://github.com/bradAGI/awesome-cli-coding-agents).
- [awesome-workspace-intelligence](https://github.com/RollNuts/awesome-workspace-intelligence) — contribution fork for an [upstream listing proposal](https://github.com/chistiq/awesome-workspace-intelligence/pull/2).

Each repository's README explains how to get started, its limitations, and its usage rights.

## Follow the work

If a project is useful to you, **star that repository** to keep it handy. Use **Watch → Custom** for the updates you want.

Bug reports and corrections are welcome in the relevant repository's Issues. Please report security problems through that repository's **Security → Report a vulnerability**, and keep credentials and personal information out of public issues.
