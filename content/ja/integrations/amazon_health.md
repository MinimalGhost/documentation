---
categories:
- aws
- cloud
- log collection
- notification
dependencies: []
description: AWS のサービス健全性イベントをほぼリアルタイムに監視。
doc_link: https://docs.datadoghq.com/integrations/amazon_health
draft: false
git_integration_title: amazon_health
has_logo: true
integration_id: amazon-health
integration_title: AWS Health
integration_version: ''
is_public: true
kind: インテグレーション
manifest_version: '1.0'
name: amazon_health
public_title: Datadog-AWS Health インテグレーション
short_description: AWS のサービス健全性を監視。
version: '1.0'
---

## 概要

AWS Health は、AWS のリソース、サービス、アカウントの状態をリアルタイムに可視化します。このインテグレーションを有効にすると、AWS Health サービスイベントが Datadog に表示されます。

{{< img src="integrations/amazon_health/awshealthevent.png" alt="AWS 健全性イベント" popup="true">}}

**注**: このインテグレーションは、AWS のビジネスサポートプランまたはエンタープライズサポートプランのお客様に対してのみ機能します。

## セットアップ

### インストール

[Amazon Web Services インテグレーション][1]をまだセットアップしていない場合は、最初にセットアップします。

### メトリクスの収集

1. AWS Health のデータを収集するには、次の権限を [Datadog IAM ポリシー][2]に追加します。詳細については、AWS Web サイト上の [Health ポリシー][3]を参照してください。

    | AWS アクセス許可                    | 説明                                      |
    | --------------------------------- | ------------------------------------------------ |
    | `health:DescribeEvents`           | すべての健全性イベントを一覧表示するために使用されます。                 |
    | `health:DescribeEventDetails`     | 健全性イベントに関する詳細情報を取得します。     |
    | `health:DescribeAffectedEntities` | 健全性イベントの影響を受ける AWS エンティティを取得します。|

2. [Datadog - AWS Health インテグレーション][4]をインストールします。

## 収集データ

### メトリクス

AWS Health インテグレーションには、メトリクスは含まれません。

### イベント

AWS Health インテグレーションには、AWS Personal Health Dashboard にあるイベントが含まれています。これには、未解決の問題、スケジュール設定されたメンテナンス、アカウント通知などが含まれます。

### サービスのチェック

AWS Health インテグレーションには、サービスのチェック機能は含まれません。

## トラブルシューティング

ご不明な点は、[Datadog のサポートチーム][5]までお問合せください。

[1]: https://docs.datadoghq.com/ja/integrations/amazon_web_services/
[2]: https://docs.datadoghq.com/ja/integrations/amazon_web_services/#installation
[3]: https://docs.aws.amazon.com/health/latest/ug/controlling-access.html
[4]: https://app.datadoghq.com/integrations/amazon-health
[5]: https://docs.datadoghq.com/ja/help/