**如何安装git**
由于我使用的是windows系统，所以直接到[官网](https://git-scm.com/downloads)下载了安装程序，具体安装程序参考廖雪峰的文章[安装Git](https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496)。

**如何使用git （常用命令解释）** 以下参考 梦想行人 博文 [Git 常用命令列表](https://www.cnblogs.com/ldj3/p/9172804.html)
* 常用
   `$ git remote add origin git@github.com:yeszao/dofiler.git         # 配置远程git版本库
$ git pull origin master                                          # 下载代码及快速合并 
$ git push origin master                                          # 上传代码及快速合并
$ git fetch origin                                                # 从远程库获取代码

$ git branch                                                      # 显示所有分支
$ git checkout master                                             # 切换到master分支
$ git checkout -b dev                                             # 创建并切换到dev分支
$ git commit -m "first version"                                   # 提交

$ git status                                                      # 查看状态
$ git log                                                         # 查看提交历史

$ git config --global core.editor vim                             # 设置默认编辑器为vim（git默认用nano）
$ git config core.ignorecase false                                # 设置大小写敏感
$ git config --global user.name "YOUR NAME"                       # 设置用户名
$ git config --global user.email "YOUR EMAIL ADDRESS"             # 设置邮箱`
* 创建版本库
	`$ git clone <url>                 # 克隆远程版本库
$ git init                        # 初始化本地版本库`
* 修改和提交
`$ git status                      # 查看状态
$ git diff                        # 查看变更内容
$ git add .                       # 跟踪所有改动过的文件
$ git add <file>                  # 跟踪指定的文件
$ git mv <old> <new>              # 文件改名
$ git rm <file>                   # 删除文件
$ git rm --cached <file>          # 停止跟踪文件但不删除
$ git commit -m “commit message”  # 提交所有更新过的文件
$ git commit --amend              # 修改最后一次提交`
* 查看提交历史
 `$ git log                         # 查看提交历史
$ git log -p <file>               # 查看指定文件的提交历史
$ git blame <file>                # 以列表方式查看指定文件的提交历史`
* 撤消
 `$ git reset --hard HEAD           # 撤消工作目录中所有未提交文件的修改内容
$ git reset --hard <version>      # 撤销到某个特定版本
$ git checkout HEAD <file>        # 撤消指定的未提交文件的修改内容
$ git checkout -- <file>          # 同上一个命令
$ git revert <commit>             # 撤消指定的提交`
* 分支与标签
`$ git branch                      # 显示所有本地分支
$ git checkout <branch/tag>       # 切换到指定分支或标签
$ git branch <new-branch>         # 创建新分支
$ git branch -d <branch>          # 删除本地分支
$ git tag                         # 列出所有本地标签
$ git tag <tagname>               # 基于最新提交创建标签
$ git tag -a "v1.0" -m "一些说明"  # -a指定标签名称，-m指定标签说明
$ git tag -d <tagname>            # 删除标签

$ git checkout dev                # 合并特定的commit到dev分支上
$ git cherry-pick 62ecb3`
* 远程与本地合并
`$ git remote -v                   # 查看远程版本库信息
$ git remote show <remote>        # 查看指定远程版本库信息
$ git remote add <remote> <url>   # 添加远程版本库
$ git remote remove <remote>      # 删除指定的远程版本库
$ git fetch <remote>              # 从远程库获取代码
$ git pull <remote> <branch>      # 下载代码及快速合并
$ git push <remote> <branch>      # 上传代码及快速合并
$ git push <remote> :<branch/tag-name> # 删除远程分支或标签
$ git push --tags                 # 上传所有标签`


