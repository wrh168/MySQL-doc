#状态比较


      untracked: 文件未被加入的版本库中.
  unmodified: 文件未被修改过.
    modified: 文件已经被修改过了.
    staged: 准备好, 可以提交到版本库中了.

状态
删除文件恢复

有时候, 我们不小心把文件给删除了. 想恢复这个文件时, 需要用到下面的命令.

我现在把仓库里的README这个文件给删除了. 然后再使用ls命令查看文件, 看看这个文件是否还存在.

$ rm README
$ ls
$ ls -al

    1
    2
    3

文件已经被删除了, 这是我们使用linux基本命令去查看文件是不是还存在这个目录中.现在我们使用git去查看一下现在仓库是什么状态

$ git status

    1

发现这个文件是误删了, 我们想把它恢复回来, 现在我们有办法吗? 如果没有将这个文件提交到仓库里, 我们是没有办法将它恢复的.

$ git checkout README

    1

然后我们再用ls查看一下文件是否存在.

$ ls -al

    1

再查看git仓库是状态

$ git status

    1

说明, 只要将文件提交到git仓库中
版本回退

什么叫版本, 一次提交就相当于一个版本. 如果更准确的说是提交的回退. 每一次提交都会将修改的状态提交到仓库中保存着, 这些信息都保存那里呢?都保存在.git的目录下.

如果想回退到上次提交的版本, 那么需要使用git reset命令.

$ git reset --hard commitID

    1

注意: 使用这个命令后,再使用git log命令不会查看到所有log的相关信息, 那么我们没有办法获取到后一个提交的CommitID.

$ git log

    1

在这里我们需要使用git reflog命令查看后一次提交的CommitID, 如果已经有了后一次提交的CommitID, 那么我们需要使用git reset命令恢复到前面提交版本.

$ git reflog

    1

从仓库中删除文件

如果将文件从仓库中删除这个文件, 需要使用git rm.

$ git rm filename

    1

这只是做了删除操作, 但没有真正的从仓库中删除, 我们只要将删除再做一次提交到仓库.

$ git commit

    1

从版本库中忽略文件

如果在我们的仓库目录里会产生三方的临时垃圾文件或是

$ touch .gitignore
版本之间对比

$ git diff

$ git diff commitID1 commitID2
什么是patch

patch多指补丁的意思, 在这里更多的指程序有一些bug, 需要我们进行fixed, 那fixed源码文件就是patch.

patch实际上是保存两个文件的差异.
git生成patch

$ git format-patch -p1

    1

git 打patch

$ git am patch-name

    1
