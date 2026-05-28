# カリキュラム設計書

ワークショップ全体の設計判断・章ごとの構成・進行ペースをまとめる作業ドキュメント。

## 設計判断ログ

| 項目 | 判断 | 理由 |
|---|---|---|
| 言語 | 日本語 | 国内学生コミュニティ向け。日本語ライブハンズオンはニッチが空いている。 |
| 環境 | Google Colab 中心 | 環境差分を最小化、GPU 無料枠で完走可能な規模に設計。 |
| ライブラリ | `numpy` + `torch` を主軸 | 「from scratch」のブランド維持。応用編では実用性のため Transformers 等も使用可。 |
| 数式 | 出す（直感と比喩で補強） | 学術的な誠実さを保ちつつ、文系出身者でも追える設計。 |
| 章の独立性 | 各章独立で完結 | 途中参加・つまみ食い受講を許容。ただし参照モデルは前章成果物を流用可能にする。 |
| 強化学習 | 独立章として扱う | 他章への統合だと本質が圧縮されすぎる。 |
| 記憶 | 独立章として扱う | エージェント時代の重要トピック。RAG とは別問題として整理。 |
| 教材作成プロセス | AI を使わず一次実装 | 解像度の担保。AI 補助は最終的なレビュー段階のみ。 |
| リリース戦略 | 形成過程編 4 章を一括リリース、応用編は都度公開 | 完成形のストーリーが伝わる単位で出す。 |

## Phase 1: 形成過程編

### 章 1: 事前学習 (Pre-training)

- **目標**: トークナイザから Transformer ブロック、学習ループ、生成までを一気通貫で実装し、「LLM が次トークンを予測するとはどういうことか」を説明できる。
- **想定所要**: 受講者 4-6 時間 / 作成者 2 週間程度
- **キー概念**: tokenization, embedding, self-attention, multi-head attention, positional encoding, causal mask, cross-entropy loss, AdamW, autoregressive generation
- **成果物**: 小規模データセット（TinyStories 等）で学習した動く GPT 風モデル

### 章 2: ファインチューニング (Fine-tuning)

- **目標**: 事前学習モデルを特定タスクに適応させる仕組みを実装し、SFT / Instruction Tuning / LoRA の違いを説明できる。
- **想定所要**: 受講者 3-5 時間
- **キー概念**: SFT, instruction tuning, chat template, LoRA / QLoRA, catastrophic forgetting
- **成果物**: 章 1 のモデルを指示追従タスクで FT したもの

### 章 3: 強化学習 (RLHF / DPO / GRPO)

- **目標**: 「人間が好む応答」をモデルに学習させる仕組みを RLHF / DPO / GRPO の系譜で実装し、それぞれの違いと使い所を説明できる。
- **想定所要**: 受講者 5-7 時間
- **キー概念**: reward model, PPO の最小実装, DPO の損失関数, GRPO, KL divergence による安定化
- **成果物**: 簡易報酬モデル + DPO で好み学習させたミニモデル

### 章 4: 推論 (Inference)

- **目標**: 学習済みモデルから効率よくテキストを生成するための手法を実装し、サンプリング戦略・KV キャッシュ・量子化を説明できる。
- **想定所要**: 受講者 3-5 時間
- **キー概念**: greedy / top-k / top-p / temperature, beam search, KV cache, speculative decoding, INT8 / INT4 量子化
- **成果物**: KV キャッシュ実装で生成速度を改善したモデル

## Phase 2: 応用編

### 章 5: Tool Use

- **目標**: LLM が外部関数を呼び出して動作を拡張する仕組みを実装し、ReAct / function calling / MCP の関係を説明できる。
- **キー概念**: function calling, ReAct, JSON schema による tool 定義, MCP

### 章 6: RAG (Retrieval-Augmented Generation)

- **目標**: 外部知識を検索して LLM の応答に活用する仕組みを実装し、embedding / vector store / re-ranking の役割を説明できる。
- **キー概念**: embedding model, vector DB, chunking strategy, hybrid search, re-ranker

### 章 7: 記憶 (Memory)

- **目標**: 長期記憶を持つエージェントの設計を実装し、context window / 要約記憶 / エピソード記憶 / vector memory の使い分けを説明できる。
- **キー概念**: short-term / long-term memory, summarization-based memory, episodic memory, agentic memory

## 1 章あたりの作成サイクル

| ステップ | 期間目安 | 内容 |
|---|---|---|
| 1. 論文リーディング | 2-3 日 | 章のキー論文 5 本を読み、要点ノートを残す |
| 2. AI なしで最小実装 | 2-3 日 | `walkthrough.ipynb` の原型を numpy + torch で書く |
| 3. 教材化 | 2-3 日 | 理論 MD → walkthrough → exercise の順で整える |
| 4. 公開 & FB 回収 | 1-2 日 | コミュニティに出してフィードバックを取り込む |

## オープン論点

- ライセンス（MIT? CC-BY? デュアル?）
- データセット選定（TinyStories / WikiText / 日本語コーパスのどれを軸にするか）
- ハンズオン中の質問対応形式（Discord? GitHub Issues?）
- 各章の論文 5 本の確定（章ごとに別ドキュメントへ）
