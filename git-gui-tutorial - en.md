准备：
1、git 2.19.1  https://git-scm.com/download/win
2、repo address： https://github.com/FrankFrankWei/git-basic-tutorial
3、配置已经完成
准备：

#1. clone from master


#2. add file

#3. life cycle of new file:
新建文件的生命周期：
```seq
new file->Staged: git add
Note left of Staged: more modifies
Staged-->new file: git reset HEAD file
Staged->Committed: git commit
Note right of Committed: rollback
Committed->Pre Commit: git reset --[modes] commitid
```

修改文件的生命周期：
```seq
old file->Modified:edit / delete
Note left of Modified: undo
Modified-->old file: git checkout -- file
Modified->Staged: git add
Note left of Staged: more modifies
Staged-->Modified: git reset HEAD file
Staged->Committed: git commit
Note right of Committed: rollback
Committed->Pre Commit: git reset --[modes] commitid
```
reset有三种模式：soft | mixed | hard

#4. life cyle of old file:
