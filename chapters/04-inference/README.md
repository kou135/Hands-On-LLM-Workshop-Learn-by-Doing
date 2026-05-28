# 章 4: 推論 (Inference)

> Phase 1 / 形成過程編

## 章の目標

- 学習済みモデルからテキストを「速く・賢く」生成するための仕組みを理解する
- サンプリング戦略（greedy / top-k / top-p / temperature）の違いを説明し、使い分けられる
- KV キャッシュ・量子化・speculative decoding がなぜ効くのかを説明できる

## 前提知識

- 章 1〜3 の完了（特に章 1 の attention 計算）

## 想定所要時間

- 受講者: 3-5 時間

## 参照論文（候補・要確定）

- [ ] Holtzman et al., "The Curious Case of Neural Text Degeneration" (top-p, 2020)
- [ ] Pope et al., "Efficiently Scaling Transformer Inference" (2022)
- [ ] Leviathan et al., "Fast Inference from Transformers via Speculative Decoding" (2023)
- [ ] Dettmers et al., "LLM.int8(): 8-bit Matrix Multiplication for Transformers at Scale" (2022)
- [ ] TBD（KV cache 圧縮系: TurboQuant / QuantSpec など）

## 構成

- `theory.md`
- `walkthrough.ipynb`
- `exercise.ipynb` / `solution.ipynb`
- `references/`

## 成果物

- KV キャッシュを自前実装して naive 実装比で速度向上を確認
- 量子化前後の精度 vs 速度トレードオフを測ったレポート

## 作成者向け TODO

- [ ] 論文 5 本確定（特に量子化系は新しめのものを選ぶ）
- [ ] KV cache を「ない実装 → ある実装」の差分で見せる演習設計
- [ ] Colab で測れる規模の速度ベンチ設計
