# RollNuts

I build developer tools and turn personal projects into runnable examples and technical notes.

個人開発で作った仕組みを、実行できるコードと技術記事にしています。

## Try the latest / まず試せるもの

**Veripsa Core → local MCP（試作）** — Rustを変更する前に、同じTauriコマンドにつながるTypeScriptの確認先と曖昧さを調べる2ツールです。固定snapshotを使う、読み取り専用の実験です。

[コード・実行手順](https://github.com/RollNuts/zenn-content/tree/f08bec5e302b68513c0d352f64c7629b60d50c83/examples/core-local-mcp) · [日本語の解説（GitHub全文／Zenn公開待ち）](https://github.com/RollNuts/zenn-content/blob/62557b0347b1fd11fbaa699095e3b2d455fcc41d/articles/tauri-command-contract-graph.md)

## Main projects / 主なプロジェクト

| Project | What you can explore | Current status |
| --- | --- | --- |
| [Veripsa Core](https://github.com/RollNuts/veripsa) | Content-free PR traffic control: structural references and decision state, without retained source or diff bodies. [Design boundary](https://github.com/RollNuts/veripsa/blob/main/docs/PRODUCT_FACTS.md#f-013-content-free-storage-boundary) · [Try local evaluation](https://github.com/RollNuts/veripsa/blob/main/docs/OFFLINE_EXAMPLE.md) · [日本語の再現手順](https://note.com/rollnuts/n/n8e700225687d). | Source-available; hosted GitHub App is suspended. |
| [Mihassei News / 未発生新聞](https://github.com/RollNuts/mihassei-news) | A fictional satire newspaper built with Python, static pages, and Cloudflare Workers. [Read it](https://veripsa.com) or build it locally. | Active project; local build needs no API credentials. |

## Technical writing / 技術記事

[Zenn](https://zenn.dev/veripsa) — Japanese implementation and operations notes on Git, Python, RSS, and static sites.

[記事の更新をRSSで購読 / Subscribe via RSS](https://zenn.dev/veripsa/feed)

- [git branch --mergedに出ない取り込み済みブランチを見分ける――556本を整理した実例](https://zenn.dev/veripsa/articles/github-branch-cleanup-squash-556)
- [創作上の2031年をRSSに流さない――静的サイトで3つの日時を分ける](https://zenn.dev/veripsa/articles/fiction-date-rss-static-site)
- [Article sources](https://github.com/RollNuts/zenn-content) — maintained through Zenn's GitHub integration.

## Reference repositories / 検証・参照用

- [ai-pr-collision-lab](https://github.com/RollNuts/ai-pr-collision-lab) — historical PR-collision recordings and a local pricing-test fixture. Current engine development is in Veripsa Core.
- [awesome-cli-coding-agents](https://github.com/RollNuts/awesome-cli-coding-agents) — reference fork. Current curation and submissions belong [upstream](https://github.com/bradAGI/awesome-cli-coding-agents).
- [awesome-workspace-intelligence](https://github.com/RollNuts/awesome-workspace-intelligence) — contribution fork for an [upstream listing proposal](https://github.com/chistiq/awesome-workspace-intelligence/pull/2).

Each repository's README explains how to get started, its limitations, and its usage rights.

## Follow the work

If a project is useful to you, **star that repository** to keep it handy. Use **Watch → Custom** for the updates you want.

Bug reports and corrections are welcome in the relevant repository's Issues. Please report security problems through that repository's **Security → Report a vulnerability**, and keep credentials and personal information out of public issues.
