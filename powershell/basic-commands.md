[study-notes](../README.md) > [PowerShell](README.md) > 基本コマンド

---

## 基本コマンド一覧
よく使うPowerShellのコマンドのメモ。  
必要に応じて追記していく。
### Set-Location
現在の作業ディレクトリを変更するコマンドレット

### New-Item
新しいファイルやフォルダーを作成するコマンドレット

### Out-File
指定したファイルにデータを書き込むコマンドレット

### Get-Item
指定したパスのファイルやフォルダーの情報を取得するコマンドレット

### Get-Content
指定したファイルの内容を表示するコマンドレット

### Test-Path
指定したパスが存在するかどうかを確認するコマンドレット


## 例：Git用のフォルダおよびファイルを作成する
```bash
## C:\github\study-notes に移動する
Set-Location C:\github\study-notes
```


```bash
# カレントフォルダ（C:\github\study-notes\）にgitフォルダを作成する
New-Item -Path git -ItemType Directory
```


```bash
# Out-FileでREADME.mdを中身あり（ヒアドキュメント）の内容で作成する
# （中身はbasic-commands.mdに書く）
@'
# Gitメモ

Gitに関するコマンドや知識をまとめる。

---

## 📋 内容

- [基本コマンド](basic-commands.md)

'@ | Out-File -FilePath git\README.md -Encoding UTF8
```


```bash
# gitフォルダー内のREADME.mdのファイル情報を見る
Get-Item .\git\README.md
```


```bash
# gitフォルダー内のREADME.mdのファイルの中身を見る
Get-Content .\git\README.md
```


```bash
# Out-Fileでbasic-commands.mdを中身あり（ヒアドキュメント）の内容で作成する
@'
# 基本コマンド

よく使うGitコマンドのメモ。  
必要に応じて追記していく。

---

## 📦 状態確認
git status

（それ以外は後で追記する）
'@ | Out-File -FilePath git\basic-commands.md -Encoding UTF8
```


```bash
# C:\github\study-notes\git\basic-commands.md が存在するか確認する（True / False）
Test-Path C:\github\study-notes\git\basic-commands.md
```


```bash
# C:\github\study-notes\git\basic-commands.mdのファイルの中身を見る
Get-Content .\git\README.md
```
