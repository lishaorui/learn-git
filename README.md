echo "# learn-git" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/lishaorui/learn-git.git
git push -u origin master
…or push an existing repository from the command line
git remote add origin https://github.com/lishaorui/learn-git.git
git push -u origin master







## Github

## 添加ssh key

使用sshkey来访问github，可以一劳永逸，不用每次都输入用户名密码，具体步骤也很简单。也可以参考github官方的[操作说明](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)。

1. 在本地机器生成key

   ```sh
   ssh-keygen -t rsa -b 4096 -C "github_account@email"
   ```

   > Generating public/private rsa key pair.
   > Enter file in which to save the key (/Users/lsr/.ssh/id_rsa):
   > /Users/lsr/.ssh/id_rsa already exists.
   > Overwrite (y/n)? y
   > Enter passphrase (empty for no passphrase):
   > Enter same passphrase again:
   > Your identification has been saved in /Users/lsr/.ssh/id_rsa.
   > Your public key has been saved in /Users/lsr/.ssh/id_rsa.pub.

2. 生成后会提示保存的路径，默认保存在``/Users/lsr/.ssh/id_rsa.pub``

3. 将id_rsa.pub中内容复制到github的[添加ssh key页面](https://github.com/settings/ssh/new)

4. 然后就可以愉快的开启github之路了。