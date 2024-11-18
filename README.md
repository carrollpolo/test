## 如何使用GitHub上传文件

### 上传文件的极简工作流程

#### `git add .` ——将所有更改过的文件添加到暂缓区

#### `git commit -m` ——将修改部分推送到本地仓库

#### `git push`—— 将本地仓库的更改推送到远程仓库(GitHub服务器)

### 上传文件的具体工作流程

#### 1. 首先进入某一个特定的文件夹，如`test`, 然后使用`git init`创建`git`文件
![alt text](https://github.com/carrollpolo/test/blob/master/images/image.png)

#### 2. 将文件添加到`staging area`,以便为下一次提交`commit`做准备
使用`git add .`推送所有的文件到本地仓库的暂缓区(staging area)，或者使用`git add **.cpp`推送某个特定的文件到本地仓库的暂缓区(staging area)。
![alt text](https://github.com/carrollpolo/test/blob/master/images/image1.png)

#### 3. 输入本次的提交说明,提交更改到本地仓库
`git commit -m "任意的提交信息"`将提交更改到本地仓库
![alt text](https://github.com/carrollpolo/test/blob/master/images/image2.png)

#### 4. 关联GitHub仓库
在`GitHub`中新建一个`repository`,复制仓库地址
![alt text](https://github.com/carrollpolo/test/blob/master/images/image4.png)
![alt text](https://github.com/carrollpolo/test/blob/master/images/image5.png)
![alt text](https://github.com/carrollpolo/test/blob/master/images/image6.png)

在本地仓库中，使用`git remote add`命令将远程仓库链接到本地仓库
    git remote add origin https://github.com/carrollpolo/test.git
#### 5. 将本地仓库推送到GitHub服务器
`git push`将本地仓库更改推送到远程仓库

    git push -u origin main

出现了下列问题,因为推送到了错误的分支(事实上,我的GitHub远程分支只有`master`)
![alt text](https://github.com/carrollpolo/test/blob/master/images/image3.png)
我们可以使用`git branch`查看远程仓库的分支，避免推送失败
![alt text](https://github.com/carrollpolo/test/blob/master/images/image7.png)
