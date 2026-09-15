# TeeTools — アバター ヘルスチェック

🇺🇸 [English README is here](README.md)

VRChatアバターによくあるパフォーマンス・アップロードの問題をスキャンし、
初心者でも分かりやすいレポートを出します。何が見つかったか、実際に気にする
べきかどうか、次に何をすればいいかまで教えてくれます。

TeeToolsシリーズの第一弾ツールです。

## インストール方法（VCC経由）

1. TeeToolsのリポジトリをVCCに追加してください（追加用リンクはメインリポジトリの
   READMEまたはindexを参照）。
2. VCCでアバタープロジェクトを開きます。
3. パッケージ一覧から「TeeTools - Avatar Health Check」を探し、Addをクリックします。

## 使い方

Unityのメニューバーから `TeeTools > Avatar Health` を開きます。アバターの
ルートGameObjectを「Target Avatar」欄にドラッグし、Scanをクリックしてください。

ツール自体にも右上に言語切り替え（English / 日本語）がついています。この
READMEはあくまでセットアップ手順の説明用です。

## 補足

- VRChat SDKへの依存は明記していません。PhysBone・PhysBone Collider・
  VRCAvatarDescriptorのチェックはリフレクションで行っているため、SDKが
  入っていないプロジェクトでもインストール・動作でき、該当チェックのみ
  スキップしてその旨を表示します。
- ポリゴン数・マテリアル数・テクスチャサイズなどのしきい値は目安の値で、
  `AvatarHealthCheck.cs` 内の `HealthCheckConfig` にまとまっています。
  自由に調整してください。
