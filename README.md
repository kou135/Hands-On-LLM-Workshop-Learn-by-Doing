# Hands-On LLM Workshop: Learn by Doing

LLM の「中身」をゼロから手で作って理解するためのハンズオンワークショップ教材。

## このワークショップの目的

- **メインターゲット**: LLM の内部構造を「自分の言葉で説明できる」レベルまで解像度を上げたい学生・若手エンジニア。
- **学習スタイル**: 各章で「論文 → 理論の噛み砕き → 最小実装 → 自分で実装演習」のサイクルを回す。
- **ライブラリ方針**: `numpy` + `torch` を主軸に、ブラックボックス化を避ける。Hugging Face Transformers 等の高レベル抽象は応用編まで原則使わない。

## 対象レベル

- Python の基本構文が読める
- 偏微分・行列積など高校〜大学初級レベルの数学に抵抗がない（数式は出すが必ず直感と比喩で補強する）
- 機械学習・深層学習の事前知識は不要

## カリキュラム概要

ワークショップは 2 部構成。詳細は [CURRICULUM.md](./CURRICULUM.md) を参照。

### Phase 1: 形成過程編（最初のリリース対象）

LLM が「どう作られているか」を、データ準備から学習済みモデルになるまで通しで体験する。

1. [事前学習 (Pre-training)](./chapters/formation/01-pretraining/)
2. [ファインチューニング (Fine-tuning)](./chapters/formation/02-finetuning/)
3. [強化学習 (RLHF / DPO / GRPO)](./chapters/formation/03-reinforcement-learning/)
4. [推論 (Inference)](./chapters/formation/04-inference/)

### Phase 2: 応用編（順次更新）

学習済みの LLM を「どう使い倒すか」を、最小実装から本格的なエージェント化まで段階的に扱う。

5. [Tool Use](./chapters/application/05-tool-use/)
6. [RAG (Retrieval-Augmented Generation)](./chapters/application/06-rag/)
7. [記憶 (Memory)](./chapters/application/07-memory/)

## 各章の構成

すべての章は以下の節を持つ：

| 節 | 内容 |
|---|---|
| 章の目標 | この章を終えると何が説明できるようになるか |
| 前提知識 | 直前までの章 / 外部リソース |
| 参照論文 | 章ごとに 5 本程度（一次資料を必ず読む） |
| 理論 | 比喩 → 数式 → 直感の 3 段で噛み砕く |
| ハンズオン | 講師による実装ウォークスルー (`walkthrough.ipynb`) |
| 演習 | 穴埋め形式の実装課題 (`exercise.ipynb` + `solution.ipynb`) |
| 参考リンク | 発展リソース・関連論文 |

## 実行環境

**Google Colab を推奨環境とする**（無料 GPU 枠で完走できる規模に設計）。

ローカル実行も可能だが、サポート優先度は Colab が先。

## 進め方の前提

- 教材作成者は **AI による生成に頼らず**、各章で論文 5 本を読み込んだ上で実装と解説を行う。
- 「from scratch」を名乗る以上、Hugging Face Transformers の `from_pretrained` で済ませる箇所を作らない（応用編では実用性のために使う）。

## ライセンス

未定（v0.1 リリース前に決定）。
