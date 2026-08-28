# IBM Z x AWS Hybrid Cloud Skill

IBM Z と AWS を組み合わせたハイブリッドクラウドの設計、構築、運用を支援するエージェントスキルです。IBM Z と AWS の役割分担、接続性、セキュリティ、モダナイゼーションを、最新の公式ドキュメントに基づいて検討します。

## 対象領域

- インフラ / コンピュート: z/OS LPAR、z/VM、Amazon EC2、Amazon EKS、Amazon ECS
- ネットワーク / 接続性: AWS Direct Connect、Site-to-Site VPN、OSA-Express、HiperSockets、Transit Gateway
- データベース / データ統合: Db2 for z/OS、IMS、Amazon RDS、DynamoDB、AWS DataSync、AWS DMS
- ストレージ: DS8000、VSAM、Amazon S3、Amazon EBS、Amazon FSx
- セキュリティ / コンプライアンス: RACF、Crypto Express、AWS IAM、AWS KMS、Security Hub
- アプリケーション / ミドルウェア: CICS、IBM MQ、WAS on Z、AWS Lambda、Amazon API Gateway
- Web サーバー / API 連携: z/OS Connect EE、IBM API Connect、Amazon API Gateway
- 監視 / 運用: OMEGAMON、Instana、Amazon CloudWatch、AWS Systems Manager
- 移行 / モダナイゼーション、コスト最適化

## 前提条件

- AWS の最新情報を確認する AWS MCP Server
- IBM Z の公式ドキュメントを検索・参照する IBM Z 用 MCP Server
- アーキテクチャ図を生成する場合は draw.io MCP Server

MCP Server を利用できない場合も、一般的な設計原則、確認事項、実装ステップの提案には利用できます。ただし、サービス仕様、リージョン可用性、製品サポート状況は公式ドキュメントで別途確認してください。

## 利用方法

このスキルを有効にしたエージェントへ、相談したい内容を伝えてください。必要に応じて対象領域と環境情報を確認し、IBM Z と AWS の両面から助言します。

```text
z/OS 上の CICS アプリケーションを AWS の API Gateway 経由で公開したい。
推奨アーキテクチャ、セキュリティ対策、実装手順を教えてください。
```

```text
IBM Z と AWS Transit Gateway を Site-to-Site VPN で接続する場合の
可用性、BGP、暗号化、MTU の推奨設定を確認したい。
```

## 利用フロー

1. 相談対象の領域を選択します。複数領域を同時に扱えます。
2. z/OS バージョン、利用ミドルウェア、AWS サービス、フェーズ、制約、ゴールを必要な範囲で確認します。
3. AWS および IBM の公式ドキュメントから最新情報を収集します。
4. アーキテクチャ、推奨構成、リスク、実装ステップ、参考資料を整理して提示します。
5. 必要に応じて、draw.io で編集可能なアーキテクチャ図を生成します。

## 回答内容

回答には通常、次の内容が含まれます。

- IBM Z 側と AWS 側の役割分担、および接続方式
- サービス選定、設定方針、セキュリティ対策
- 可用性、性能、ライセンス、ネットワークに関するリスク
- 優先度順の実装ステップ
- IBM および AWS の公式ドキュメントへの参照

## アーキテクチャ図

図の生成を希望する場合、IBM Z の LPAR、z/VM、z/OS、ミドルウェア、DS8000 と、AWS のリージョン、VPC、サブネット、マネージドサービスを含む draw.io 図を作成します。AWS サービスは公式アイコンを使用し、Direct Connect や VPN、MQ、API などの接続経路とプロトコルを明記します。

生成後の図は draw.io 上でレイアウト変更やコンポーネント追加を行い、PNG、SVG、PDF などへエクスポートできます。

## 設計上の注意

- AWS の仕様は変更されるため、設計判断の前に最新の公式ドキュメントを確認します。
- z/OS のバージョン、PTF レベル、製品構成により利用可否が変わるため、環境情報を確認してから判断します。
- IBM Z の MLC、IPLA などのライセンス費用は複雑です。コスト見積もりは IBM 担当者と確認してください。
- ハイブリッド接続では、認証、暗号化、ネットワーク分離を必須の設計要素として扱います。
- 大規模な移行や統合は、リスクを抑えるため段階的に進めます。

## ネットワーク設定の支援

z/OS Communications Server と AWS Site-to-Site VPN の接続では、IKEv2、AES256-GCM-16、DH Group 14 以上、PFS、有効な DPD、BGP 冗長化、MTU の調整などを検討します。具体的なパラメータ例、ファイアウォール要件、z/OS 側の確認コマンドはスキル定義に含まれています。

## スキル定義

エージェント向けの詳細な実行手順、回答テンプレート、draw.io の作図規則、ネットワーク設定例は [SKILL.md](SKILL.md) を参照してください。