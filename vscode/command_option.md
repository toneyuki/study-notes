[study-notes](../README.md) > [Visual Studio Code](README.md)  > コマンドオプション

---

# Visual Studio Code コマンドラインインターフェース
VSCodeのcodeコマンドのオプションで気になったものを書く

## 📖 参考サイト
- Documentation for Visual Studio Code
  - https://code.visualstudio.com/docs/configure/command-line

## オプション
#### (file)
開くファイルを選択（複数選択可能）

#### (folder)
開くフォルダを選択（複数選択した場合はマルチルートワークスペースが作成される）

#### -n or --new-window
前回のセッションを復元せず、新しく開く

#### -
標準入力を受けとって、新しく開くファイルに入れる

#### --list-extensions
インストール済みの拡張機能を表示

#### --update-extensions
インストール済みの拡張機能を更新して終了


#### --profile
- 📖 参考
  - https://code.visualstudio.com/docs/configure/profiles
  - https://code.visualstudio.com/docs/configure/profiles#_doc-writer-profile-template

サイトに記載されている通り、以下のテンプレートプロファイルが最初から入っていた。
- Python
- Data Science
- Doc Writer
- Node.js
- Angular
- Java General
- Java Spring

（日本語UIでは、[ファイル]タブ > [ユーザー設定] > [プロファイル]で開く）


## コマンド例
フォルダを開く
```bash
code C:\github\study-notes\vscode\
```

前回セッションを使用せず新規ファイルで開く（旧メモ帳代わり）
```bash
code -n
```

テンプレファイルの内容で新しく開く（コピペしてから開けばいい気もするが...）
```PowerShell
$template_path = "C:\github\study-notes\template\README.md"
Get-Content $template_path -Encoding utf8 | code -

# -オプションを指定すると、他のオプションが効いていないように見える
#（-nオプションを指定しているのに前回のセッションが開いてしまう。ファイル名を指定しても標準入力の内容が入らない。）
echo "hello world!" | code - -n "README.md"
```

Doc Writerプロファイルでフォルダを開く
```bash
code C:\github\study-notes\vscode\ --profile "Doc Writer" -n
```
