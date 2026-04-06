[study-notes](../README.md) > [GitHub CLI](README.md) > 初期設定

---

# GitHub CLI 初期設定

`gh auth login` コマンドで、GitHubへの認証を行う。

## 📋 参考  
1. [GitHub CLI | GitHubをコマンドラインで操作しよう](https://cli.github.com/manual/gh_auth_login)  
2. [GitHub CLI 公式インストールガイド (Windows)](https://github.com/cli/cli/blob/trunk/docs/install_windows.md#winget)  
3. [GitHubへの認証について - GitHub ドキュメント](https://docs.github.com/ja/authentication/keeping-your-account-and-data-secure/about-authentication-to-github#https)  

---

## 🔐 認証方式

今回は **HTTPSのブラウザフロー認証** を使用する。  
（PATやSSH鍵は使用しない）

---

## ▶️ 実行コマンド

```bash
gh auth login --clipboard --git-protocol https --web
```
オプションメモ
・--clipboard
ワンタイムコードをクリップボードにコピーする（貼り付けが楽）
--git-protocol
Gitの通信方式をHTTPSに固定（対話入力を省略）
--web
Enter押下でブラウザのDevice Activation画面を開く

## 📋 実行ログ
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>

```text
>gh auth login --clipboard --git-protocol "https" --web
? Authenticate Git with your GitHub credentials? Yes

! One-time code (○○○○-○○○○) copied to clipboard
Press Enter to open https://github.com/login/device in your browser...
✓ Authentication complete.
- gh config set -h github.com git_protocol https
✓ Configured git protocol
✓ Logged in as toneyuki
! You were already logged in to this account

>gh auth status
github.com
  ✓ Logged in to github.com account toneyuki (keyring)
  - Active account: true
  - Git operations protocol: https
  - Token: gho_************************************
  - Token scopes: 'gist', 'read:org', 'repo', 'workflow'
```
</details>
