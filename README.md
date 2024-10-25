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

### 版本回退
1.--soft 保留暂存区和工作区
`git reset --soft ${commit ID}`

2.--hard 舍弃暂存区和工作区
`git reset --hard ${commit ID}`

3.--mixed 舍弃暂存区,保留工作区
`git reset --mixed ${commit ID}`

4.查看所有提交记录
`git reflog`

### 比较差异
1.默认情况比较工作区和暂存区的差异
`git diff`

2.比较暂存区和仓库的差异
`git diff --cached`

3.比较工作区和仓库之间的差异
`git diff ${commit ID}`

4.比较两个版本之间的差异
`git diff ${commit ID} ${commit ID}`

### 删除文件
1.先从工作区删除文件，再同步暂存区，再提交
`rm ${rmFileName}`
`git add ${rmFileName} / git add .`
`git commiit -m ${remove description}`

2.git rm 命令同时删除暂存区和工作区文件，再提交
`git rm ${rmFileName}`
`git commiit -m ${remove description}`