# 每一个git项目的准备工作
## 0. Previous
```bash
apt-get install git
ssh-keygen -t rsa #三次回车

```
### 复制`id_rsa.pub`文件内容到github
登录github -> Accounting settings图标 -> SSH key -> Add SSH key -> 填写SSH key的名称（可以起一个自己容易区分的），然后将拷贝的 .ssh/id\_rsa.pub文件内容粘帖 -> add key 按钮添加。

## 1. 在github创建一个仓库 project_name

## 2. 本地创建相同名字的仓库 project_name
撰写代码
```bash
git init
git add . # 提交所有变动文件
git commit -m "first commit"
git remote add origin git@github.com:ai-charlie/project_name.git
git branch -M main
git push -u origin main
```

## 3. 每一次提交
```bash
git pull # 拉取
git add . # 提交所有变动文件
git commit -m "XXX commit"
git push -u origin main
```

## 4. 删除远程仓库
```bash
git remote rm origin
```

## 5. 添加`git-lfs`大文件存储
use Updated git hooks.
Git LFS initialized.
```bash
apt-get install git-lfs
git lfs install
```

### 重置到某一次历史提交状态

#### 0 设置远程项目允许强制推送
设置 -> 仓库 -> 受保护的分支 -> 允许强制推送

#### 1 重置到某一历史提交状态
git reset --hard 复制提交SHA

#### 强制推送
git push origin main --force