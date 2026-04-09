[study-notes](../README.md) > AWS

---

# AWSメモ

AWSに関して興味のあるサービスをまとめる。

---

## 📖 AWS 用語集
- https://docs.aws.amazon.com/ja_jp/glossary/latest/reference/glos-chap.html
 - エッジロケーション：AWSのためのデータセンター。ユーザーの近くのエッジロケーションにコンテンツをキャッシュして高速化する

## 📋 内容

### IAM Identity Center
- 

### Amazon Cognito
- https://aws.amazon.com/jp/cognito/
- Web・モバイルアプリケーションのサインアップ/サインイン/アクセスコントロールの提供
- Amazon DynamoDB、Amazon S3、AWS Lambdaなどのサービスに対する安全なロールベースのサポート
#### 💰 コスト
- https://aws.amazon.com/jp/cognito/pricing/
  - 

### Amazon SNS
- 多要素認証やOTPのためのSMSメッセージを送信する
- https://aws.amazon.com/jp/sns/sms-pricing/

### 🌐 CloudFront（クラウドフロント）
- https://aws.amazon.com/jp/cloudfront/
機能：
セキュリティ：AWS Web Application Firewall (WAF)との連携
セキュリティ：HTTPS経由の配信。

#### 💰 コスト
- 従量課金と定額料金（月額）がある。
- 従量課金
  - https://aws.amazon.com/jp/cloudfront/pricing/pay-as-you-go/
    - 従量課金制
      - データ転送量
      - リクエスト数
    - アクセスが少なければ低コスト
- 定額料金
  - https://aws.amazon.com/jp/cloudfront/pricing/?nc=sn&loc=3


### 🔐 AWS Certificate Manager (ACM)
- https://docs.aws.amazon.com/ja_jp/acm/latest/userguide/acm-overview.html
セキュリティ：証明書とキーを作成
#### 💰 コスト
- https://aws.amazon.com/jp/certificate-manager/pricing/?nc=sn&loc=3
- https://docs.aws.amazon.com/acm/latest/userguide/acm-services.html
  - ACMが発行するパブリック証明書はACM 統合サービスで利用でき、無料で発行される。
    ・Elastic Load Balancing
    ・Amazon CloudFront
    ・Amazon Elastic Kubernetes Service
    ・Amazon Cognito
    ・AWS Elastic Beanstalk
    ・AWS App Runner
    ・Amazon API Gateway
    ・AWS Nitro Enclaves
    ・AWS CloudFormation
    ・AWS Amplify
    ・Amazon OpenSearch Service
    ・AWS Network Firewall
- https://aws.amazon.com/jp/certificate-manager/pricing/?nc=sn&loc=3
- https://aws.amazon.com/jp/private-ca/pricing/
  - エクスポート可能な証明書（AWS外等で使用）は料金がかかる
  - ACMでPrivate CA（AWS上で動く社内向け認証局）を利用する場合もかなりかかる
#### ⚠ 制約
- https://docs.aws.amazon.com/ja_jp/AmazonCloudFront/latest/DeveloperGuide/cnames-and-https-requirements.html
  - CloudFrontでACM証明書を使用するには、米国東部 (バージニア北部) リージョン (us-east-1) の証明書である必要あり
  
### 📢 AWS Polly
- テキストを音声に変換するサービス。多言語に対応している。
#### 💰 コスト
- https://aws.amazon.com/jp/polly/pricing/?nc=sn&loc=4
- https://docs.aws.amazon.com/polly/latest/dg/voice-engines-polly.html
- エンジンによって異なる（料金は100万文字あたり）
  - Standard TTS Cost（連結合成方式を採用した標準エンジン）：4.00 USD
  - Neural TTS Cost（標準音声よりも高品質なNTTS）：16.00 USD
  - Long-form TTS Cost（テキストを解釈し長文に対して一貫性のある読み上げ）：100.00 USD
  - Generative TTS Cost（最新AI技術による高品質な読み上げ）：30.00 USD
- メモ
  - Amazon Translateの翻訳機能と組み合わせ多言語対応
