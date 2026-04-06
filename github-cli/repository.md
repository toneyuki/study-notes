[study-notes](../README.md) > [GitHub CLI](README.md) > リポジトリ作成

---

# GitHub CLI リポジトリ作成

`gh auth login` コマンドで、GitHubへの認証を行う。

## 📋 参考  
[GitHub CLI | Take GitHub to the command line](https://cli.github.com/manual/gh_repo_create)

---

## ▶️ 実行コマンド（すでにローカルリポジトリとなるフォルダ構成がある場合）

```bash
gh repo create git --private --source=<リポジトリに追加する親フォルダパス> --remote=<リモートリポジトリ名> --push
```
オプションメモ
・--public / --private
*リポジトリを公開設定にするか、非公開設定にするか*＜重要＞
・--source=
ローカルリポジトリとなるフォルダパス
・--remote=
リモートリポジトリ名。通常はorigin。
・--push
ローカルコミットを新しいリポジトリにプッシュする


## ▶️ 実行コマンド（ローカルリポジトリも新規に作成する場合）【今回はこちらを実行】

```bash
cd <作成するローカルリポジトリの親フォルダ>
gh repo create <作成するリポジトリ・フォルダ名> --private --clone --description <リポジトリの説明> --add-readme
```
オプションメモ
・--public / --private
*リポジトリを公開設定にするか、非公開設定にするか*＜重要＞
・--clone
作成したリモートリポジトリをローカルフォルダにクローンする
・--description <リポジトリの説明>
リポジトリ作成時に設定可能
・--add-readme
作成したリポジトリにREADME.mdを作成する。

gh repo create iam-access-key-activator --private --clone --description "IAMユーザーアクセスキー有効化 承認基盤（AMP for Email + AWS Lambda）" --add-readme

## 📋 実行ログ（ローカルリポジトリも新規に作成する場合）
<details>
<summary>🚩 実際の実行ログ（クリックで展開）</summary>

```text
C:\github>cd C:\github

C:\github>gh repo create iam-access-key-activator --private --clone --description "IAMユーザーアクセスキー有効化 承認基盤（AMP for Email + AWS Lambda）" --add-readme
✓ Created repository toneyuki/iam-access-key-activator on github.com
  https://github.com/toneyuki/iam-access-key-activator
Cloning into 'iam-access-key-activator'...

C:\github>cd iam-access-key-activator

C:\github\iam-access-key-activator>dir
 ドライブ C のボリューム ラベルは OS です
 ボリューム シリアル番号は E455-0EA3 です

 C:\github\iam-access-key-activator のディレクトリ

2026/04/06  16:19    <DIR>          .
2026/04/06  16:19    <DIR>          ..
2026/04/06  16:19               117 README.md
               1 個のファイル                 117 バイト
               2 個のディレクトリ  343,056,019,456 バイトの空き領域

C:\github\iam-access-key-activator>gh browse
```
（gh browseでブラウザ上で作成したリポジトリが開かれる）
</details>
