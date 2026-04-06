[study-notes](../README.md) > [GitHub CLI](README.md) > インストール

---

# GitHub CLI インストール

Windows標準のパッケージマネージャー **winget** を使用してインストールする。

---

## ▶️ インストール

```bash
winget install --id GitHub.cli
```

## ✅ インストール確認
```bash
gh --version
```
　・結果
```text
gh version 2.89.0 (2026-03-26)
https://github.com/cli/cli/releases/tag/v2.89.0
```

## 📋 参考
[GitHub CLI 公式インストールガイド (Windows)](https://github.com/cli/cli/blob/trunk/docs/install_windows.md#winget)


## 📋 実行ログ
コマンド実行時、以下の利用規約同意が表示された。（Microsoft Storeの利用規約とリージョン取得）
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>

```text
>winget install --id GitHub.cli
'msstore' ソースでは、使用する前に次の契約を表示する必要があります。
Terms of Transaction: [https://aka.ms/microsoft-store-terms-of-transaction](https://aka.ms/microsoft-store-terms-of-transaction)
ソースが正常に機能するには、現在のマシンの 2 文字の地理的リージョンをバックエンド サービスに送信する必要があります (例: "US")。

すべてのソース契約条件に同意しますか?
[Y] はい  [N] いいえ: y

見つかりました GitHub CLI [GitHub.cli] バージョン 2.89.0
このアプリケーションは所有者からライセンス供与されます。
Microsoft はサードパーティのパッケージに対して責任を負わず、ライセンスも付与しません。
ダウンロード中 [https://github.com/cli/cli/releases/download/v2.89.0/gh_2.89.0_windows_amd64.msi](https://github.com/cli/cli/releases/download/v2.89.0/gh_2.89.0_windows_amd64.msi)
  ██████████████████████████████  14.0 MB / 14.0 MB
インストーラーハッシュが正常に検証されました
パッケージのインストールを開始しています...
インストールが完了しました
```
</details>
