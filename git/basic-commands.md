[study-notes](../README.md) > [Git](README.md) > 基本コマンド

---

# 基本コマンド
よく使うGitコマンドのメモ。  
必要に応じて追記していく。

---

## 参考
- [Git - git-status Documentation](https://git-scm.com/docs/git-status)
- [Git - git-add Documentation](https://git-scm.com/docs/git-add)
- [Git - git-restore Documentation](https://git-scm.com/docs/git-restore)
- [Git - git-stash Documentation](https://git-scm.com/docs/git-stash)

---


## 📦 状態確認
作業ツリーの状態を表示する。
変更差分のあるファイルや、未追跡ファイル（untracked）を確認できる。
```bash
git status
```

## 📦 ステージング
変更・追加されたファイルをインデックス（ステージング）に追加する。
ステージングは「次のコミット内容の準備」。
### すべてステージング
```bash
git add .
```

### ファイル指定でステージング
```bash
git add <ファイル名>
```

### ステージングを取り消す
```bash
git restore --staged <ファイル名>
```

## 📦 変更を破棄（ワークツリーの復元）
ファイルをHEADの状態に戻す。
**元に戻せないため注意**
- ファイルを指定して捨てる
```bash
git restore <ファイル名>
git restore <ファイル名> --worktree

```

## 📦 変更を一時退避（stash）
作業途中の変更を一時保存して、作業ツリーをクリーンにする。

### 退避する
```bash
git stash
```

### 一覧を確認
```bash
git stash list
```

### 退避内容を復元（一覧からは残す）
```bash
git stash apply
```

### 退避内容を復元（一覧からは削除）
```bash
git stash pop
```

（後々追記する）
