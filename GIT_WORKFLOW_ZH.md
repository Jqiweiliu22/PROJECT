# GitHub 修改记录与两人协作

仓库：https://github.com/Jqiweiliu22/PROJECT

本文件夹已连接 main 分支。请在 VS Code 中打开本文件夹继续开发。Git 记录每次提交的版本：保存文件只会产生待提交修改，不会自动生成历史或上传。

## 每次完成一个修改

1. 保存并验证程序。
2. 在 VS Code 左侧“源代码管理”检查差异，暂存这次修改的文件。
3. 填写具体说明，例如 Fix Windows API tests，点击提交。
4. 点击“同步更改”或“推送”。
5. 在 GitHub 的 Commits 页面确认记录出现。

也可以在项目终端运行：

```powershell
git status
git diff
git add app.py
git commit -m "Describe the actual change"
git push
```

把 app.py 替换为实际修改的文件，可以列出多个文件；新文件也要暂存。不要提交密码、密钥、缓存或虚拟环境。

## 两人协作

仓库所有者在 GitHub Settings → Collaborators 添加组员。组员接受邀请后，在自己的电脑克隆：

```powershell
git clone https://github.com/Jqiweiliu22/PROJECT.git
cd PROJECT
```

每人使用自己的 GitHub 登录及 Git 姓名、邮箱。每次开始工作前，先确保自己的待提交修改已经处理，再执行 git pull --ff-only 获取最新版本；完成后提交并推送。尽量避免同时修改同一段代码。有冲突时共同核对，不要强制推送覆盖对方。

## 检查连接和历史

```powershell
git remote -v
git status -sb
git log --oneline -5
```

远程应为上述 PROJECT 仓库。提交并推送完成后，本次修改不应仍留在待提交列表，main 应与 origin/main 同步。

VS Code 已配置自动获取远程状态；它不会自动提交或上传文件。初次导入只记录压缩包进入仓库，不能补回此前的开发历史。两人的后续真实工作应分别提交，更新 AI-LOG 和贡献声明。
