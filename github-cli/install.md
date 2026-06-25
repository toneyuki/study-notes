[study-notes](../README.md) > [GitHub CLI](README.md) > インストール

---

# GitHub CLI インストール

---

## ▶️ インストール

### Windows
Windows標準のパッケージマネージャー **winget** を使用してインストールする。
```bash
winget install --id GitHub.cli
```

### Linux（DebianのUbuntu）
Ubuntuでは、APTを使用してインストールする。
```
(type -p wget >/dev/null || (sudo apt update && sudo apt install wget -y)) \
	&& sudo mkdir -p -m 755 /etc/apt/keyrings \
	&& out=$(mktemp) && wget -nv -O$out https://cli.github.com/packages/githubcli-archive-keyring.gpg \
	&& cat $out | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
	&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
	&& sudo mkdir -p -m 755 /etc/apt/sources.list.d \
	&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
	&& sudo apt update \
	&& sudo apt install gh -y
```

## ✅ インストール確認
```bash
gh --version
```
・結果
```text
gh version 2.95.0 (2026-06-17)
https://github.com/cli/cli/releases/tag/v2.95.0
```

## 📋 参考
[GitHub CLI 公式インストールガイド (Windows)](https://github.com/cli/cli/blob/trunk/docs/install_windows.md#winget)<br>
[GitHub CLI 公式インストールガイド (Linux & BSD)](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)



## 📋 実行ログ
### Windows
Windowsでコマンド実行時、以下の利用規約同意が表示された。（Microsoft Storeの利用規約とリージョン取得）
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

### Linux（DebianのUbuntu）
通常のinstallのみだとUbuntu標準リポジトリ版は古い場合があるため、基本は公式APTリポジトリを追加する方法がおすすめとのこと
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>

```text
$ (type -p wget >/dev/null || (sudo apt update && sudo apt install wget -y)) \
        && sudo mkdir -p -m 755 /etc/apt/keyrings \
        && out=$(mktemp) && wget -nv -O$out https://cli.github.com/packages/githubcli-archive-keyring.gpg \
        && cat $out | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
        && sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
        && sudo mkdir -p -m 755 /etc/apt/sources.list.d \
        && echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
        && sudo apt update \
        && sudo apt install gh -y
2026-06-25 15:31:38 URL:https://cli.github.com/packages/githubcli-archive-keyring.gpg [4528/4528] -> "/tmp/tmp.uW9naDePWk" [1]
Get:1 https://cli.github.com/packages stable InRelease [3917 B]
Get:2 https://cli.github.com/packages stable/main amd64 Packages [354 B]
Hit:3 http://security.ubuntu.com/ubuntu resolute-security InRelease
Hit:4 http://archive.ubuntu.com/ubuntu resolute InRelease
Hit:5 http://archive.ubuntu.com/ubuntu resolute-updates InRelease
Hit:6 http://archive.ubuntu.com/ubuntu resolute-backports InRelease
Fetched 4271 B in 2s (2800 B/s)
14 packages can be upgraded. Run 'apt list --upgradable' to see them.
Upgrading:
  gh

Summary:
  Upgrading: 1, Installing: 0, Removing: 0, Not Upgrading: 13
  Download size: 14.7 MB
  Space needed: 3994 kB / 1021 GB available

Get:1 https://cli.github.com/packages stable/main amd64 gh amd64 2.95.0 [14.7 MB]
Fetched 14.7 MB in 1s (22.5 MB/s)
(Reading database ... 43057 files and directories currently installed.)
Preparing to unpack .../archives/gh_2.95.0_amd64.deb ...
Unpacking gh (2.95.0) over (2.46.0-4) ...
Setting up gh (2.95.0) ...
Processing triggers for man-db (2.13.1-1build1) ...

```
</details>