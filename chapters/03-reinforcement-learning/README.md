# 章 3: 強化学習 (RLHF / DPO / GRPO)

> Phase 1 / 形成過程編

## 章の目標

- 「人間が好む応答」をモデルに学習させる仕組みを 3 系統（RLHF / DPO / GRPO）で理解する
- 報酬モデルの役割と、KL 制約による安定化を説明できる
- DPO が「報酬モデルなしで RLHF と等価な目的を達成する」ロジックを直感と数式の両面で語れる

## 前提知識

- 章 2（ファインチューニング）の完了
- 強化学習の基本（policy / reward / value）は章内で最小限カバーするが、Sutton 本の最初 1-2 章レベルがあると楽

## 想定所要時間

- 受講者: 5-7 時間（章中で最重量）

## 参照論文（候補・要確定）

- [ ] Christiano et al., "Deep Reinforcement Learning from Human Preferences" (2017)
- [ ] Schulman et al., "Proximal Policy Optimization Algorithms" (PPO, 2017)
- [ ] Rafailov et al., "Direct Preference Optimization" (DPO, 2023)
- [ ] Shao et al., "DeepSeekMath: Pushing the Limits of Mathematical Reasoning..." (GRPO, 2024)
- [ ] DeepSeek-R1 technical report (2025)

## 構成

- `theory.md`
- `walkthrough.ipynb`
- `exercise.ipynb` / `solution.ipynb`
- `references/`

## 成果物

- 簡易報酬モデル + DPO で好み学習させたミニモデル
- RLHF と DPO の挙動比較ノート

## 作成者向け TODO

- [ ] 論文 5 本確定
- [ ] PPO を「最小限の数式 + 玩具実装」で見せる範囲を決める（深入りすると章が破綻する）
- [ ] DPO 損失の導出を「比喩 → 数式 → コード」の順に組み立てる
- [ ] GRPO は「R1 で注目された理由」中心に圧縮するか深掘りするか方針決定
