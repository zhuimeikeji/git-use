# git使用备注

#### 新建项目

        echo "# git-use" >> README.md
        git init
        git add README.md
        git commit -m "first commit"
        git remote add origin git@github.com:zhuimeikeji/git-use.git
        git push -u origin master


#### 已有项目

        git remote add origin git@github.com:zhuimeikeji/git-use.git
        git push -u origin master


#### 关联多个平台的SSH KEY

1. 生成指定SSH KEY

        ssh-keygen -t rsa -C "备注"

2. 进入SSH目录，创建CONFIG

        cd ~/.ssh
        touch config

3. 打开CONFIG，填写对应站点数据

        Host github.com
        HostName github.com
        User git
        IdentityFile c:\Users\super\.ssh\id_rsa

        Host gitee.com
        HostName gitee.com
        User git
        IdentityFile c:\Users\super\.ssh\gitee_id_rsa

User 用户名可以都用 git

#### 同一个项目提交到多个平台

        git remote add github git@github.com/youname/youprojectname.git
        git remote add coding git@coding.net/youname/youprojectname.git
        git push github master
        git push coding master

通常用origin作为远程仓库的名字，它只是个名字而已，你可以换成你喜欢的名字。例如我这里换成了github和coding

#### 更多待更新

