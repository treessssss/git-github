# SSH密钥

一般我们从github上下载文件时，只要复制HTTPS的网址，git clone即可下载下来。当我们想要SSH下载时，就需要设置SSH。

- 检查自己git config是否配置

  首先查看自己的git config，可以通过命令行`git config --global --list`查看 

-  没有user.name和user.email没有值的话，我们也可以先配置，命令行配置如下 
  -  git config --global user.name "这里换上你的用户名" 
  -  git config --global user.email "这里换上你的邮箱" 
-   命令行输入`ssh-keygen -t rsa -C "这里换上你的邮箱" `，执行生成你的SSHkey
- 然后一直回车即可
- 打开电脑C盘users里的 Administrator 里面的.SSH文件
  - 里面有三个文件，其中id_rsa为密钥
  - id_rsa.pub为公钥，打开公钥全选复制里面的内容
- 在GitHub中关联ssh
  
  - 进入GitHub的个人设置setting，找到 【SSH and GPG keys】 , 然后点击新增SSH ，tilte输入对公钥的备注， 下面的key就粘贴上一步生成的id_rsa.pub内的内容 
- 完成后就可以SSH下载了