# 章 5: Tool Use

> Phase 2 / 応用編

## 章の目標

- LLM が外部関数を呼び出して動作を拡張する仕組みを実装できる
- ReAct / function calling / MCP の関係と進化を説明できる
- 「なぜ tool use がエージェントの基礎になるのか」を語れる

## 前提知識

- Phase 1（形成過程編）の完了が望ましいが、応用編から入っても可
- 学習済みモデルをロードして推論できる環境

## 参照論文（候補・要確定）

- [ ] Yao et al., "ReAct: Synergizing Reasoning and Acting in Language Models" (2022)
- [ ] Schick et al., "Toolformer: Language Models Can Teach Themselves to Use Tools" (2023)
- [ ] Anthropic, "Building Effective Agents" (2024)
- [ ] MCP 仕様（Model Context Protocol）
- [ ] TBD

## 構成

- `theory.md`
- `walkthrough.ipynb`
- `exercise.ipynb` / `solution.ipynb`
- `references.md`

## 成果物

- 自前関数（電卓・天気 API など）を tool 化して LLM から呼ばせるデモ
- MCP サーバの最小実装

## 作成者向け TODO

- [ ] Phase 1 完走後に着手
- [ ] 論文 5 本確定
- [ ] Phase 1 のモデルで tool use できるか、または外部 API（Anthropic / OpenAI）を使うかの方針決定
