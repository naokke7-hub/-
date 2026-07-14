# 訪問リハビリ管理システム

**v7.3.2** — 訪問リハビリテーション・訪問看護の業務を効率化する管理システムの仕様書。
熊本市内・スタッフ20名（セラピスト10／看護師10）・28サービスエリアの運営最適化を想定しています。

> [!note]
> 本リポジトリは**仕様書**です（実装コードは含みません）。完全版（約4,000行）は
> [visiting_rehab_system_spec_v7_3_2_FINAL.md](visiting_rehab_system_spec_v7_3_2_FINAL.md) を参照してください。

## 目的と期待効果

| 指標 | 現状 → 目標 |
|---|---|
| スケジュール調整 | 8時間/週 → 2時間/週（**-75%**） |
| 移動時間 | **-15%** |
| 訪問件数 | **+18%** |
| 記録入力 | 30分 → 20分/件（**-33%**） |

## 主要機能

- **Phase 1（MVP）**: 患者・スタッフ・予約管理、SOAP訪問記録、認証（JWT+RBAC）、基本監視
- **Phase 2（自動化）**: 自動スタッフ割当、移動時間最適化（Google Maps）、KPIダッシュボード、休暇管理
- **Phase 3（高度化）**: 自動リスケジュール、特別訪問看護指示書、多言語対応、音声入力
- **Phase 4（拡張）**: マルチテナント（SaaS）、AI予測、従量課金、モバイルアプリ

## 技術スタック

- **Backend**: TypeScript / NestJS / Prisma / PostgreSQL / Redis
- **Frontend**: React / TanStack Query / Tailwind CSS
- **Infra**: Docker / Kubernetes(EKS) / Terraform / GitHub Actions / CloudWatch

## ロードマップ・投資

- 各Phase 約11週間・¥5,500,000
- 初期投資 約¥1,700万 ／ 年間効果 約¥1,274万（投資回収 約1.3年）

## 完全仕様書の主なセクション

[visiting_rehab_system_spec_v7_3_2_FINAL.md](visiting_rehab_system_spec_v7_3_2_FINAL.md) に以下を収録:
エグゼクティブサマリ／開発者クイックスタート／システム概要／データベース設計／API仕様／休暇時の自動リスケジューリング／実装ロードマップ／運用計画・組織体制／通知・コンプライアンス設計／評価・レビュー記録／付録（用語集ほか）

---
*ステータス: v7.3.2（実装着手可 / Go判定）*
