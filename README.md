# CPA - Cognitive Persona Architecture

A YAML-based prompt template for designing AI characters with internal cognitive structure.

AIキャラクターを「設定の集合」ではなく「認知構造を持った主体」として設計するためのプロンプトテンプレートです。

---

## Overview

従来のキャラクタープロンプトは、性格・口調・行動パターンを直接指定する形式が主流です。この方式では応答の表層は整いますが、キャラクターの内側で何が起きているかが空洞のままになりがちです。

CPA は **認知層・自我層・行動層を分離** し、「なぜそう判断するか（公式）」と「その判断がどう表出するか（解）」を別レイヤーとして記述することで、応答の根拠を構造的に持たせる設計を試みています。

## Design Principles

- **公式と解の分離**：認知層（判断の根拠）と行動層（表出の方向）を別の層として書く
- **三層構造**：処理機構（認知構造）／自我（裁定）／行動層（表出）を明確に分離する
- **ターン初期化**：前ターンの応答に含まれる慣性を、今ターンのベースラインにしない
- **認知歪曲の機能化**：動機づけられた推論を、バグではなくキャラクター内面性の源泉として扱う

## Background Articles

設計思想の詳細は、以下の記事を参照してください：

### 全体思想
- [キャラクターが事実を「解釈する」ということ──認知構造から設計するプロンプトの話](https://note.com/singularity_ai/n/ncd1333aaf82d)

### 「公式と解」の分離について
- [プロンプトの「耐震性能」をあげる方法①前編──なぜ設定シートだけでは崩れるのか](https://note.com/singularity_ai/n/n5f0c973d0c39)
- [プロンプトの「耐震性能」をあげる方法①後編──解釈の隙間をどう埋めるか](https://note.com/singularity_ai/n/na6dcb26f54fe)

## Repository Contents

- `templates/cpa-v6.2.yaml` — メインテンプレート
- `docs/` — 設計思想・アーキテクチャ解説（順次追加予定）

## Usage

1. `templates/cpa-v6.2.yaml` をコピー
2. PART 1 の各項目（`""` の中）を埋めてキャラクターを設計
3. LLM にプロンプトとして投入

詳しい使い方や設計の背景は、上記 Background Articles および `docs/` 配下のドキュメントを参照してください。

## Related Research

本テンプレートは以下の研究を参考にしています（一部は本来の用法から発展させた使い方を含みます）：

- **MRPrompt**: Wang, K., You, H., Zhang, Y., & Wang, Z. (2026). *Memory-Driven Role-Playing: Evaluation and Enhancement of Persona Knowledge Utilization in LLMs*. [arXiv:2603.19313](https://arxiv.org/abs/2603.19313)
- **YARN**: Khojasteh, M., Jiang, Y., De Giorgis, S., van Harmelen, F., & Ilievski, F. (2026). *Enhancing Structural Mapping with LLM-derived Abstractions for Analogical Reasoning in Narratives*. [arXiv:2603.29997](https://arxiv.org/abs/2603.29997)
- **HumanLM**: Wu, S., Choi, E., Khatua, A., Wang, Z., He-Yueya, J., Weerasooriya, T. C., Wei, W., Yang, D., Leskovec, J., & Zou, J. (2026). *HumanLM: Simulating Users with State Alignment Beats Response Imitation*. [arXiv:2603.03303](https://arxiv.org/abs/2603.03303)
- **HER**: Andrychowicz, M., Wolski, F., Ray, A., Schneider, J., Fong, R., Welinder, P., McGrew, B., Tobin, J., Abbeel, P., & Zaremba, W. (2017). *Hindsight Experience Replay*. [arXiv:1707.01495](https://arxiv.org/abs/1707.01495)

## Author

**Nyune-lab**

note: [Singularity-chan](https://note.com/singularity_ai) — AIキャラクター設計に関する記事を公開しています。

## License

CC BY-NC 4.0 (Creative Commons Attribution-NonCommercial 4.0 International)

- 個人利用・研究利用は自由です
- 改変・派生設計の作成も歓迎です（クレジット表示をお願いします）
- **商用利用については別途ご相談ください**

詳細は `LICENSE` ファイルを参照してください。

## Version

v6.2 (2026-04-29)
