## git遇到的问题汇总

1. 无法向github推送空的文件夹

2. 首先我们查看github的仓库。如下图所示。

   ![](https://raw.githubusercontent.com/zkydrx/images/master/test.png)

   仓库中并没有test文件夹。

3. 然后我们在 git bush中执行了下图中的所有命令。

   ![](https://raw.githubusercontent.com/zkydrx/images/master/test1.png)

   - 首先进入本地仓库mybooksnote

   - mkdir test (创建一个名字为test的文件夹)

   - git add -A (将tracked 和untracked 所有改变的文件添加到缓存)

   - git commit -am 'test add emtpy folder'(提交所有的添加到仓库中。)

   - git push https://github.com/zkydrx/myBooksNote.git master(将本地的仓库推送到远程。push后为远程的仓库地址也可以这样写

     github@github.com:zkydrx/myBooksNote.git master)

4. 进行完以上动作以后再去github中看下是否添加进去了。结果如下图。

   ![](https://raw.githubusercontent.com/zkydrx/images/master/test2.png)

   发现并没有把本地新增的仓库推送给远程的仓库。

5. 继续进行下面的步骤。

   ![](https://raw.githubusercontent.com/zkydrx/images/master/createFile.png)

    - cd test (进入test文件夹)
    - touch README.md(创建README.md的文件)
    - git add -A (将tracked and untracked 所有的改变的文件添加进缓存)
    - git commit -am 'add files'(提交添加的缓存到本地仓库)
    - cd .. (退回到上一级目录。)

   ![](https://raw.githubusercontent.com/zkydrx/images/master/push1.png)

   - git push git@github.com:zkydrx/myBooksNote.git master (将本地仓库推送到远程的仓库。更新所有的改变。生成一个新的版本。)

6. 下面到github代码托管仓库中看看是否有变化。

   ![](https://raw.githubusercontent.com/zkydrx/images/master/change1.png)

   发现代码托管仓库中的确有了一个新的文件夹test而且test文件夹里面确实有README.md文件。

   ## 总结

   - github无法接受空的文件夹推送。如果要有空文件夹要在空文件夹中添加必要的文件方可推送。