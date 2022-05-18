# 学习Git遇到的错误记录和解决方法
## push常见的错误
 * error: failed to push some refs to 'https://gitee.com/solitudegitee/learning-notes.git'
   * 解决方法是 
     * 1.想把本地完全强制推送过去就git push origin main -f
     * 2.如果想与远程代码合并，那就git pull origin main合并代码，然后再推送。

* 如果GitHub出现身份或者密码已经过期：
   * 解决方法是
     * 先去GitHub账户中，选择设置->开发人员设置->个人访问令牌->生成新令牌->然后填写表单->单击生成令牌->复制生成的令牌。
     * 然后根据不同的系统进行操作：
       * windows：
        * 从控制面板转到凭据管理器->Windows Credentials ->查找->编辑->密码替换为GitHub 个人访问令牌->完成   git:https://github.com
        * 如果您没有找到->单击"添加通用的Credentials->Internet 地址，您需要输入您的用户名和密码将是您的GitHub 个人访问令牌->单击"确定"，您就完成了git:https://github.comgit:https://github.com。
       * linux:
        * 对于 Linux，您需要使用用户名和电子邮件地址配置本地Git：
          ```
           $ git config --global user.name "your_github_username"
           $ git config --global user.email "your_github_email"
           $ git config -l
          ```
        * 配置 GIT 后，我们可以开始使用它来访问 GitHub.如果你在git命令没有弹出提示输入用户名和密码
          那么就要使用：
          ```
           $ git config --global --unset credential.helper
           $ git config --system --unset credential.helper
          ```
          来删除缓存记录。
        * 可以使用 `$ git config --global credential.helper cache`让计算机记住令牌。
         