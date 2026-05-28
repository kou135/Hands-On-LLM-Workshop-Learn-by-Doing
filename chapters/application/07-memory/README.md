# 章 7: 記憶 (Memory)

> Phase 2 / 応用編

## 章の目標

- 長期記憶を持つエージェントの設計を実装できる
- context window / 要約記憶 / エピソード記憶 / vector memory の使い分けを説明できる
- 「記憶」と「RAG」の本質的な違いを語れる

## 前提知識

- 章 5（Tool Use）と章 6（RAG）の完了

## 参照論文（候補・要確定）

- [ ] Park et al., "Generative Agents: Interactive Simulacra of Human Behavior" (2023)
- [ ] Packer et al., "MemGPT: Towards LLMs as Operating Systems" (2023)
- [ ] Zhong et al., "MemoryBank: Enhancing LLMs with Long-Term Memory" (2023)
- [ ] TBD（agentic memory 系の新しい論文）
- [ ] TBD

## 構成

- `theory.md`
- `walkthrough.ipynb`
- `exercise.ipynb` / `solution.ipynb`
- `references.md`

## 成果物

- 会話履歴を持ち、過去の発言を要約 + 検索できるエージェント
- 「context に全部入れる」「要約だけ持つ」「vector memory」の比較ベンチ

## 作成者向け TODO

- [ ] 論文 5 本確定
- [ ] MemGPT 系の OS 比喩をどこまで採用するか方針決定
- [ ] 章 6 (RAG) との境界線を明確にする（同じ vector store でも「記憶」と「知識」は使い方が違う）
