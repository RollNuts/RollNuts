# RollNuts

I use AI-assisted development to turn practical problems into developer tools, runnable examples, and inspectable technical notes.

AIと進めた個人開発を、実行できるコード・検証記録・技術記事として残しています。

## Start here / まず試せるもの

**Veripsa Core — コードの構造とGit履歴を、一緒に確かめる。**

頻繁なGitコンフリクトを減らしたくて作り始めた仕組みから、コードグラフ・Co-change・永続化の技術が生まれました。今は、他の開発者が手元で試し、結果と限界を検証できる公開資産として整えています。

[無料のローカルデモ](https://github.com/RollNuts/veripsa/tree/main/examples/structural-overlap) · [日本語ガイド](https://github.com/RollNuts/veripsa/blob/main/docs/README.ja.md) · [解析基盤とDBの役割](https://github.com/RollNuts/veripsa/blob/main/docs/ANALYSIS_ASSETS.md)

Gitのclean merge、コードグラフ、履歴上の関連、統合後の実行を4つの合成例で比較します。POSIX環境のGit＋Python 3.12で動き、追加パッケージ・モデルAPI・DBは不要です。ホスト型GitHub Appは停止中です。

## Main projects / 主なプロジェクト

| Project | What you can explore | Current status |
| --- | --- | --- |
| [Veripsa Core](https://github.com/RollNuts/veripsa) | Code graph, historical co-change, and durable PR coordination. [Local demo](https://github.com/RollNuts/veripsa/tree/main/examples/structural-overlap) · [Implementation inventory](https://github.com/RollNuts/veripsa/blob/main/docs/ANALYSIS_ASSETS.md) · [Pinned Flask evaluation](https://github.com/RollNuts/veripsa/blob/main/docs/OFFLINE_EXAMPLE.md). | Source-available; hosted GitHub App is suspended. |
| [Mihassei News / 未発生新聞](https://github.com/RollNuts/mihassei-news) | A fictional satire newspaper built with Python, static pages, and Cloudflare Workers. [Read it](https://veripsa.com) or build it locally. | Active project; local build needs no API credentials. |

## Agent integration / AIから使う実験

[Core → local MCP / Codex](https://github.com/RollNuts/zenn-content/tree/89fe0fe12258c827a9e7fc54cb12fc96401018de/examples/core-local-mcp) — a separate read-only adapter for a saved Tauri snapshot. SDK-only reproduction is model-free; optional Codex execution uses the signed-in account's allowance. [日本語の解説（Zenn）](https://zenn.dev/veripsa/articles/tauri-command-contract-graph) · [GitHub原稿](https://github.com/RollNuts/zenn-content/blob/main/articles/tauri-command-contract-graph.md).

## Technical writing / 技術記事

[Zenn](https://zenn.dev/veripsa) — Japanese implementation, code-analysis, and operations notes on Git, Python, RSS, and static sites.

[記事の更新をRSSで購読 / Subscribe via RSS](https://zenn.dev/veripsa/feed)

- [Gitでマージできたのに壊れる――コードグラフとCo-changeを4例で検証](https://zenn.dev/veripsa/articles/graph-cochange-review-benchmark) — 4つの合成例を、手元で実マージ・実行・採点する。
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
