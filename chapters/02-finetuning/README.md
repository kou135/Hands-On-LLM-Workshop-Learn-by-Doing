# 章 2: ファインチューニング (Fine-tuning)

> Phase 1 / 形成過程編

## 章の目標

- 事前学習モデルを特定タスクに適応させる仕組みを実装できる
- SFT / Instruction Tuning / LoRA の違いと使い分けを説明できる
- 「なぜ全パラメータを更新せず LoRA で十分なのか」を直感と数式の両面から語れる

## 前提知識

- 章 1（事前学習）の完了
- 章 1 で学習したモデル（or 公開済み小型モデル）

## 想定所要時間

- 受講者: 3-5 時間

## 参照論文（候補・要確定）

- [ ] Ouyang et al., "Training language models to follow instructions with human feedback" (InstructGPT, 2022)
- [ ] Hu et al., "LoRA: Low-Rank Adaptation of Large Language Models" (2021)
- [ ] Dettmers et al., "QLoRA: Efficient Finetuning of Quantized LLMs" (2023)
- [ ] TBD

## 構成

- `theory.md`
- `walkthrough.ipynb`
- `exercise.ipynb` / `solution.ipynb`
- `references/`

## 成果物

- 章 1 のモデルを指示追従タスクで SFT したもの
- LoRA アダプタを差し替えて挙動が変わることを確認するデモ

## 作成者向け TODO

- [ ] 論文 5 本確定
- [ ] FT 用データセットの選定（Dolly / 日本語 instruction データ）
- [ ] LoRA を numpy 寄りで書くか torch の `nn.Module` で素直に書くか方針決定
- [ ] catastrophic forgetting を体感させるデモを設計
