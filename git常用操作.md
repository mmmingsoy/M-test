一、基础配置
bash
# 设置用户
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"

# 初始化仓库
git init
git clone https://github.com/用户名/仓库名.git

二、日常操作
bash
# 查看状态
git status

# 添加文件
git add 文件名      # 单个文件
git add .          # 所有文件

# 提交
git commit -m "提交说明"
git commit -am "说明"  # 添加并提交

# 查看历史
git log
git log --oneline  # 简洁版

三、分支管理
bash
# 查看分支
git branch

# 创建并切换分支
git checkout -b 分支名

# 切换分支
git checkout 分支名

# 合并分支
git merge 要合并的分支名

# 删除分支
git branch -d 分支名

四、远程仓库
bash
# 添加远程仓库
git remote add origin 仓库地址

# 推送到远程
git push origin 分支名
git push          # 简写

# 从远程拉取
git pull origin 分支名
git pull          # 简写
五、撤销操作
bash
# 撤销未暂存的修改
git checkout -- 文件名

# 撤销暂存的修改
git reset HEAD 文件名

# 撤销上一次提交
git revert HEAD

六、储藏功能
bash
# 临时保存修改
git stash

# 恢复储藏
git stash pop

# 查看储藏列表
git stash list

七、常用场景

1. 开发新功能
bash
git checkout -b feature-login
# 写代码...
git add .
git commit -m "添加登录功能"
git push origin feature-login

2. 更新本地代码
bash
git checkout main
git pull origin main

3. 解决合并冲突
bash
# 手动编辑冲突文件
git add 冲突文件
# 标记已解决
git commit -m "解决冲突"
