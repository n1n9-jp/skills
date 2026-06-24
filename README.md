> **注意:** このリポジトリには Claude 向けのスキルの Anthropic による実装が含まれています。Agent Skills 標準については [agentskills.io](http://agentskills.io) を参照してください。

[![skills.sh](https://skills.sh/b/anthropics/skills)](https://skills.sh/anthropics/skills)

# スキル
スキルは、Claude が専門的なタスクのパフォーマンスを向上させるために動的に読み込む命令・スクリプト・リソースのフォルダです。スキルは、Claude に特定のタスクを繰り返し実行する方法を教えます[...]

詳細については以下を参照してください:
- [What are skills?](https://support.claude.com/en/articles/12512176-what-are-skills)
- [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [Equipping agents for the real world with Agent Skills](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

# このリポジトリについて

このリポジトリには、Claude のスキルシステムで可能なことを示すスキル群が含まれています。これらのスキルは、クリエイティブな用途（アート、音楽、デザイン）から技術的なタスク（ウェブアプリのテスト等）まで幅広く含まれます[...]

各スキルはそれぞれのフォルダ内で自己完結しており、Claude が使用する命令とメタデータを含む `SKILL.md` ファイルを持ちます。これらのスキルを参照して、自分自身のスキル作成の参考にしてください[...]

このリポジトリ内の多くのスキルはオープンソース（Apache 2.0）です。さらに、[Claude のドキュメント機能](https://www.anthropic.com/news/create-[...]) を支えるドキュメント作成・編集スキルも含まれています。

## 免責事項

**これらのスキルはデモンストレーションおよび教育目的で提供されています。** これらの機能の一部は Claude で利用可能な場合がありますが、ここにある実装や Claude から得られる振る舞いは[...]

# スキルセット
- [./skills](./skills): クリエイティブ＆デザイン、開発＆技術、企業＆コミュニケーション、ドキュメントスキルのサンプル
- [./spec](./spec): Agent Skills 仕様
- [./template](./template): スキルテンプレート

# Claude Code、Claude.ai、API で試す

## Claude Code
このリポジトリを Claude Code のプラグインマーケットプレイスとして登録するには、Claude Code で以下のコマンドを実行します:
```
/plugin marketplace add anthropics/skills
```

特定のスキルセットをインストールするには:
1. `Browse and install plugins` を選択
2. `anthropic-agent-skills` を選択
3. `document-skills` または `example-skills` を選択
4. `Install now` を選択

あるいは、直接プラグインをインストールするには:
```
/plugin install document-skills@anthropic-agent-skills
/plugin install example-skills@anthropic-agent-skills
```

プラグインをインストールしたら、そのスキル名を言及するだけでスキルを使えます。例えば、マーケットプレイスから `document-skills` プラグインをインストールした場合、Claude Code に対して次のような操作を依頼できます: [...]

## Claude.ai

これらの例示的なスキルは、Claude.ai の有料プランで既に利用可能です。

このリポジトリのスキルを使うかカスタムスキルをアップロードするには、[Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude#h_a4222fa7[...]) の手順に従ってください。

## Claude API

Anthropic の事前構築スキルを使用したり、カスタムスキルをアップロードしたりするには、Claude API を使用できます。詳しくは [Skills API Quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill) を参照してください。

# 基本的なスキルの作成

スキルは作成が簡単です — `SKILL.md` ファイル（YAML フロントマターと命令を含む）を置いたフォルダを作るだけです。このリポジトリの **template-skill** を出発点として使えます:

```markdown
---
name: my-skill-name
description: A clear description of what this skill does and when to use it
---

# My Skill Name

[Add your instructions here that Claude will follow when this skill is active]

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

フロントマターで必須なのは次の 2 項目です:
- `name` — スキルの一意の識別子（小文字、スペースはハイフン）
- `description` — スキルが何を行い、いつ使うかの完全な説明

下のマークダウン本文には、Claude がスキルが有効なときに従う命令、例、ガイドラインが含まれます。詳細は [How to create custom skills](https://support.claude.com/en/articles/12512[...]) を参照してください。

# パートナースキル

スキルは、特定のソフトウェアの使い方を Claude に学習させる優れた方法です。パートナーから素晴らしいサンプルスキルが届いた際には、ここでいくつかを紹介することがあります:

- **Notion** - [Notion Skills for Claude](https://www.notion.so/notiondevs/Notion-Skills-for-Claude-28da4445d27180c7af1df7d8615723d0)
