# UploadToGitHub
    上传项目到GitHub
### VSCode
    使用vscode上传有两种方式：

<a href="#terminal">纯终端上传</a> 使用命令

<a href="#vscode">vscode自身</a> 还是需要使用终端进行初始操作

初始操作：

<a href="#init">初始化本地仓库</a>

<a href="#remote">建立远程连接</a>

- <span id="terminal">终端上传</span>

        完整教程从初始化/创建本地仓库开始

    - 初始化/创建本地仓库
            
            登录自己的GitHub账号，创建一个项目
        <img src="./image/vscode_uploadGitHub_1.png" alt="创建GitHub项目">
            
            创建项目 看图
        <img src="./image/vscode_uploadGitHub_2.png" alt="创建GitHub项目">

            进入vscode 打开终端
        <img src="./image/vscode_uploadGitHub_3.png" alt="打开终端">

            在终端中使用 git init 初始化/创建本地仓库
        <img src="./image/vscode_uploadGitHub_4.png" alt="初始化/创建本地仓库">
    - 将项目提交到本地仓库

            首先要有项目
        <img src="./image/vscode_uploadGitHub_5.png" alt="创建项目文件">

            上一步只是创建了一个文件
            但是这个文件还不在本地仓库里
            使用 git status 可以查看文件到底在不在本地仓库里面
        <img src="./image/vscode_uploadGitHub_6.png" alt="查看文件状态">

            那么怎么才能把文件添加到本地仓库呢
            使用 git add . 可以将所有文件添加到本地仓库
            把.替换成想要添加的文件名(要加后缀)可以实现添加对应的文件
        <img src="./image/vscode_uploadGitHub_7.png" alt="添加到本地仓库">

            上面那些都完成了 就该提交到本地仓库了
            使用 git commit -m '这里面是提交说明'
        <img src="./image/vscode_uploadGitHub_8.png" alt="提交到本地仓库">

            下面就是建立远程连接了
            进入GitHub刚刚创建的那个项目
            复制界面中的那个地址
        <img src="./image/vscode_uploadGitHub_9.png" alt="复制远程连接地址">

            进入vscode中 在终端输入命令 ，
            git remote add origin 你复制的GitHub远程连接地址  建立本地仓库和GitHub项目的远程连接。
            现在就可以开始上传项目到GitHub上了 使用命令
            git push -u origin master
            有时候会出现提示输入用户名和密码，这是正常的。
        <img src="./image/vscode_uploadGitHub_10.png" alt="建立远程连接和上次项目">
    - 上传完成

            完成后的截图
            可以看到GitHub的那个项目已经变了，多了一个README.md文件
        <img src="./image/vscode_uploadGitHub_11.png" alt="完成">
    - 更新项目

            你的项目不会是完美的需要不断的更新
            那么怎么实现更新操作呢
        <img src="./image/vscode_uploadGitHub_12.png" alt="加入新的文件">

            加入的新的文件,这时候就需要更新了.
            首先还是来看看文件的状态，还记得是那条命令吗？
            git status 对!就是这条.
        <img src="./image/vscode_uploadGitHub_13.png" alt="查看文件状态">

            不出所料新加进去的文件果然是红色的
            那么使用 git add . 添加到本地仓库？
            no no no 现在是做更新操作了应该使用
            git add * 将做了更改的文件全部添加到本地仓库
            当然你要想添加指定文件也可以将*替换成文件名(要加后缀)
        <img src="./image/vscode_uploadGitHub_14.png" alt="添加更新到本地仓库">

            有提交说明当然也有更新说明，
            还是一样的使用命令
            git commit -m '这里面是更新说明'
        <img src="./image/vscode_uploadGitHub_15.png" alt="提交更新到本地仓库">

            现在又一条新的命令 git pull 拉取当前分支最新代码.
            接下来就是上传更新后的文件,会不会还是使用 git push -u origin master 呢?
            答案是不会，应该使用
            git push origin master

        <img src="./image/vscode_uploadGitHub_16.png" alt="拉取更新代码和上传更改文件">
    - 更新完成

            这里使用了一个方便查看GitHub目录结构的插件
        <img src="./image/vscode_uploadGitHub_17.png" alt="完成">

- <span id="vscode">vscode自身</span>

        这么快就到了这一步了，看来你领悟的很快嘛
        友情提示这一步是建立在已经完成了初始化本地仓库和远程连接的基础上的
    ---

    <a href="#init">初始化本地仓库</a>

    <a href="#remote">建立远程连接</a>

    ---

    - 如果你已经完成了这两个操作那么就看接下来的步骤吧

            上传和更新项目都是一样的操作
        <img src="./image/vscode_uploadGitHub_18.png" alt="添加新的文件">

            在vscode切换到分支选项
        <img src="./image/vscode_uploadGitHub_19.png" alt="切换分支">
            
            将更改的文件添加到本地仓库
        <img src="./image/vscode_uploadGitHub_20.png" alt="添加到暂存">

            提交到本地仓库，点击后会出现输入框 输入提交/更新说明
        <img src="./image/vscode_uploadGitHub_21.png" alt="提交">
        <img src="./image/vscode_uploadGitHub_22.png" alt="输入提交说明">

            按了回车后是不是觉得好了？别这样觉得不然前面的都白费了,
            明明还有一步是上传/更新到GitHub,
            这一步经常被忘，记住了
        <img src="./image/vscode_uploadGitHub_23.png" alt="上传">
    - 上传/更新完成

            可以看到多次了几张图片
        <img src="./image/vscode_uploadGitHub_24.png" alt="完成">


- <span id="init">初始化本地仓库</span>

        这一步是上传的两种方式都需要做的
        
    - 创建GitHub项目
            
            登录自己的GitHub账号，创建一个项目
        <img src="./image/vscode_uploadGitHub_1.png" alt="创建GitHub项目">
            
            创建项目 看图
        <img src="./image/vscode_uploadGitHub_2.png" alt="创建GitHub项目">

            进入vscode 打开终端
        <img src="./image/vscode_uploadGitHub_3.png" alt="打开终端">

            在终端中使用 git init 初始化/创建本地仓库
        <img src="./image/vscode_uploadGitHub_4.png" alt="初始化/创建本地仓库">
- <span id="remote">建立远程连接</span>

        这一步也是上传的两种方式都需要做的
    - 查看GitHub的远程连接地址

            创建好一个GitHub项目后会出现这样的一个界面
            复制界面中的地址
        <img src="./image/vscode_uploadGitHub_9.png" alt="复制远程连接地址">

            进入vscode中 在终端输入命令 
            git remote add origin 你复制的GitHub远程连接地址
            图中其他内容不用看 因为这是按照终端上传截的图
        <img src="./image/vscode_uploadGitHub_10.png" alt="建立远程连接">
    