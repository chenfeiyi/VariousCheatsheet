## Git cheat sheet

用来记录常用的git命令,防止遗忘


### 合并分支

首先将你需要合并的每个分支都git push一遍,防止有部分没有更新到

### 添加gitignore文件

#### 常用规则

    /mtk/ 过滤整个文件夹
    *.zip 过滤所有.zip文件
    /mtk/do.c 过滤某个具体文件

以斜杠/开头表示目录；  
以星号通配多个字符； 
以问号?通配单个字符  
以方括号[]包含单个字符的匹配列表；  
以叹号!表示不忽略(跟踪)匹配到的文件或目录；*  

#### 指定要将哪些文件添加到版本管理中    

    !src/   不过滤该文件夹
    !*.zip   不过滤所有.zip文件
    !/mtk/do.c 不过滤该文件

#### 先提交了文件而没有添加gitignore文件,可通过下面方式修改已经上传的文件

如果你的文件已经提交，而此时你才发现忘了添加.gitignore文件，不用担心，有办法，只要按照下面的步骤一一来做就可以

按顺序依次执行如下命令：  

```
    git rm -r --cache .  

    git add .  

    git commit -m ".gitignore now work"  
```

删除特定的文件夹或者文件

```
git rm -r --cache idea //删除文件夹
git rm -r --cache readme.md //删除某个文件

git add git commit git push即可
```



 

#### git添加ssh私钥并建立git连接

1. 本地生成私钥（ubuntu）

   `ssh-keygen -t rsa -C "your_email@example.com"`

2. 接着在终端输入

   `ssh-add ~/.ssh/id_rsa`

   如果成功，则会显示

   `Identity added: /Users/xxx/.ssh/id_rsa (/Users/xxx/.ssh/id_rsa)`

3. 最后，在 /Users/xxx/.ssh/ 生成两个文件，id_rsa 和 id_rsa.pub
   在终端输入：`cat /Users/xxx/.ssh/id_rsa.pub`

4. 终端就会显示你的SSH key了，直接复制就可以了。 