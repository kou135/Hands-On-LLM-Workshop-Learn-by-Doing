# 章 6: RAG (Retrieval-Augmented Generation)

> Phase 2 / 応用編

## 章の目標

- 外部知識を検索して LLM の応答に活用する仕組みを実装できる
- embedding / vector store / chunking / re-ranking それぞれの役割を説明できる
- 「いつ RAG で、いつ FT で、いつ tool use か」を判断できる

## 前提知識

- Phase 1 の完了が望ましい
- 章 5（Tool Use）の完了

## 参照論文（候補・要確定）

- [ ] Lewis et al., "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks" (RAG, 2020)
- [ ] Karpukhin et al., "Dense Passage Retrieval for Open-Domain Question Answering" (DPR, 2020)
- [ ] Gao et al., "Retrieval-Augmented Generation for Large Language Models: A Survey" (2024)
- [ ] TBD（re-ranker 系: ColBERT / BGE-reranker など）
- [ ] TBD（hybrid search 系）

## 構成

- `theory.md`
- `walkthrough.ipynb`
- `exercise.ipynb` / `solution.ipynb`
- `references.md`

## 成果物

- 自分のドキュメント（ブログ・メモなど）を embedding 化して QA できる小型 RAG
- chunking 戦略の違いで精度がどう変わるかの比較

## 作成者向け TODO

- [ ] 論文 5 本確定
- [ ] embedding モデル選定（多言語対応の小型モデルを優先）
- [ ] vector store 選定（FAISS / Chroma / SQLite-VSS）
