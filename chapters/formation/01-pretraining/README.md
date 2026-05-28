# 章 1: 事前学習 (Pre-training)

> Phase 1 / 形成過程編

## 章の目標

この章を終えると、以下を **自分の言葉で説明できる** ようになる：

- 文字列がどう「トークン」になり「ベクトル」になって Transformer に入るか
- self-attention が「文脈を見て次のトークンを予測する」とはどういう計算か
- 学習ループで何が更新され、loss が下がると何が起きているか

## 前提知識

- Python 基本構文
- Tensor の基本（shape, broadcasting）
- 偏微分の概念（厳密な式は不要）

## 想定所要時間

- 受講者: 4-6 時間
- 作成者: 2 週間（論文 3 日 + 実装 3 日 + 教材化 3 日 + FB 数日）

## 参照論文（候補・要確定）

> 最終的に 5 本に絞る。`references/` に PDF とメモを置く。

- [ ] Vaswani et al., "Attention Is All You Need" (2017)
- [ ] Radford et al., "Language Models are Unsupervised Multitask Learners" (GPT-2, 2019)
- [ ] Kaplan et al., "Scaling Laws for Neural Language Models" (2020)
- [ ] Sennrich et al., "Neural Machine Translation of Rare Words with Subword Units" (BPE, 2016)
- [ ] TBD

## 構成

- `theory.md`: 理論パート（比喩 → 数式 → 直感）
- `walkthrough.ipynb`: 講師実装ノートブック（Colab 想定）
- `exercise.ipynb`: 穴埋め演習
- `solution.ipynb`: 演習解答
- `references.md`: 参照論文と発展リソース

## 成果物

- TinyStories 程度の小規模データセットで学習した、動く GPT 風モデル（数 M パラメータ）
- 生成サンプル（loss 推移グラフ + テキスト生成結果）

## 作成者向け TODO

- [ ] 論文 5 本確定
- [ ] データセット選定（TinyStories / 日本語小コーパス）
- [ ] tokenizer の方針決定（character / byte / BPE のどれから始めるか）
- [ ] Colab 無料 GPU 枠での学習時間を実測
- [ ] `theory.md` 初稿
- [ ] `walkthrough.ipynb` 初稿（AI を使わずに書く）
- [ ] `exercise.ipynb` の穴埋めポイント設計
