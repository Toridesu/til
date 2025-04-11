## 手順
1. git log --oneline
2. git checkout <コミットID>
3. # mainブランチに切り替え
git checkout main

# mainブランチを特定のコミット時点に戻す
git reset --hard <コミットID>

# 変更をリモートに強制的にプッシュ（注意: 履歴が書き換わります）
git push --force origin main

