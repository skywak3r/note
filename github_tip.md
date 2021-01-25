github_tip

0. 参数设置

   git config --global user.name ""

   git config --global user.email ""

   + 私钥配置

     1.本地安装好git；

     2.桌面右键 Git Bash Here 打开git命令行；

     3.ssh-keygen -t rsa -C "nideyouxiang@xxx.com"  （全部按enter）；

     4.cd ~/.ssh  （如果没有执行第三步，则不会有这个文件夹）；

     5.cat id_rsa.pub   在命令行打开这个文件，会直接输出密钥；

     6.复制，打开github  ，点自己头像 >> settings >> SSH and GPG keys >>New SSH key 

     7. titile 随便写。 key里  粘贴第六步的内容；完成。

1. 基本概念

   pull_request 提交对给原仓库代码的修改，给原仓库的人审核

   merge  原仓库的人觉得不错，则会合并仓库

   issue bug提交及处理

   

   

2. git add  将工作区代码提交到暂存区  git status查看状态

   git commit -m  提交暂存区到git仓库

3. git push 提交到远程仓库

4. 