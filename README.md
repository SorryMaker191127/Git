## 使用Git

### 配置用户名和邮箱
`git config --global user.name ${userName}`
`git config --global user.email ${userEmail}`

### 创建仓库（两种方式）
1.本地创建全新的仓库
`git init`
2.从远程克隆已存在的仓库
`git clone ${url}`

### git仓库命令
1.查看当前仓库状态
`git status`

2.将文件添加到暂存区
`git add ${fileName}`
`git add *.${fileType}`
`git add .`

3.将文件从暂存区移除
`git rm --cached ${fileName}`

4.将文件提交到仓库
`git commiit -m ${commit description}`

5.查看提交记录
`git log`