一、环境配置
1.VScode下载，安装python，chinese，path intellisece, npm, npm intellisence, Vetur, Vue3 Snippets, vscode-icons, live sever 这些插件
2.配置终端 切换到cmd
3.安装前端开发工具HbuilderX https://www.dcloud.io/hbuilderx.html
4.安装小程序开发工具 https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html
二、安装git
1.安装git https://git-scm.com
2.创建远程仓库 myBlog

3.初始化本地仓库，也就是在本地myBlog文件夹下执行 git init ，执行完后会创建一个 .git 的隐藏文件
4.远程仓库和本地仓库进行关联 git remote add origin “你的远程仓库地址”
5.如果出现错误，ssh没有创建
6.先去创建秘钥 ssh-keygen,一路enter，生成秘钥
7.查看生成的秘钥 cat ~/.ssh/id_rsa.pub 
8.将秘钥写入到github上的settings下的SSH and GPG keys 下
9.推送四步骤：
git status 查看发生变化的文件
git add . 追踪所有发生变化的文件
git commit -m "备注" 提交到本地仓库
git push -u origin master （第一次提交）推送到远程仓库
git push （之后提交）
三、创建myBlog项目
1.空文件下，执行 django-admin startproject myBlog创建myBlog项目
2.给myBlog创建虚拟环境，使用 python -m venv env(env为虚拟环境名称)
3.进入虚拟环境，Windows下：.\\env\\Scripts\\activate
4.退出虚拟环境，Windows下：deactivate
5.使用VSCode打开myBlog，执行 
python manage.py startapp articles 创建articlesAPP 
python manage.py startapp users 创建usersAPP
python manage.py startapp cousers 创建cousersAPP
6.迁移 python manage.py makemigrations
python manage.py migrate
四、创建articles的model
1.创建model

2.数据库同步
3.在admin.py中注册model
五、业务逻辑

1、文章列表页，分页
2、章详情页，评论
3、全局搜索功能 Q
4、最新文章，最新评论的排行
5、按照分类，标签的一个聚类操作
6、联系我页面，发送邮件