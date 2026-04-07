[study-notes](../README.md) > [GitHub CLI](README.md) > リポジトリ公開・非公開設定

---

# GitHub CLI リポジトリ公開・非公開設定

`gh repo edit` コマンドで、リポジトリの公開設定を変更する

## 📋 参考  
[GitHub CLI | Take GitHub to the command line](https://cli.github.com/manual/gh_repo_list)（gh repo list）
[GitHub CLI | Take GitHub to the command line](https://cli.github.com/manual/gh_repo_edit)（gh repo edit）
[リポジトリの可視性を設定する - GitHub Enterprise Cloud Docs](https://docs.github.com/ja/enterprise-cloud@latest/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility)

---


## ▶️ 実行コマンド
現在のリポジトリの公開設定を確認

```bash
gh repo list
```

<details>
<summary>その他（クリックで展開）</summary>
カレント以外を指定（ownerの前にrepoは×）
</details>
```bash
gh repo list <owner>
```

```bash
gh repo list <owner/repo>
```
JSON
```bash
gh repo list --json name,description,visibility,updatedAt
```
</detail>

## 📋 実行ログ（変更前確認）
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>
INFOがprivateとなっている。
```text
>gh repo list

Showing 2 of 2 repositories in @toneyuki

NAME                               DESCRIPTION                                             INFO     UPDATED
toneyuki/study-notes               個人学習用。学びなおしと気になった技術の新規学習        private  about 11 minutes ago


> gh repo list --json name,description,visibility,updatedAt
[
  {
    "description": "個人学習用。学びなおしと気になった技術の新規学習",
    "name": "study-notes",
    "updatedAt": "2026-04-07T02:53:24Z",
    "visibility": "PRIVATE"
  }
]
</details>

## 📋 実行ログ（変更時オプション指定ミスでエラー）
**--visibilityを指定するには、--accept-visibility-change-consequencesも指定する必要があった。（サイトにも書かれてた）**
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>
INFOがprivateとなっている。
```text
> gh repo edit toneyuki/study-notes --visibility public
use of --visibility flag requires --accept-visibility-change-consequences flag

Usage:  gh repo edit [<repository>] [flags]

Flags:
...
</details>

## 📋 実行ログ（publicに変更）
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>
> gh repo edit --visibility=public --accept-visibility-change-consequences
✓ Edited repository toneyuki/study-notes
</details>


## 📋 実行ログ（変更後確認）
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>
INFOがpublicとなっている。
```text
> gh repo list

Showing 2 of 2 repositories in @toneyuki

NAME                               DESCRIPTION                                                           INFO     UPDATED
toneyuki/study-notes               個人学習用。学びなおしと気になった技術の新規学習                      public   about 1 hour ago


> gh repo list --json name,description,visibility,updatedAt
[
  {
    "description": "個人学習用。学びなおしと気になった技術の新規学習",
    "name": "study-notes",
    "updatedAt": "2026-04-07T03:52:15Z",
    "visibility": "PUBLIC"
  }
]
</details>
