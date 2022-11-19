# HEXO 多端同步

> [(79条消息) hexo多终端同步和管理_玖涯的博客-CSDN博客](https://blog.csdn.net/nineya_com/article/details/103535192)

将源码上传到仓库的另外一个分支进行同步

- 在博客目录下初始化本地仓库：git init
- 本地仓库和远程仓库对接：git remote add origin git@github.com:name.github.io.git;
- git remote -v 查看远程仓库地址，验证配置是否正确
- 创建新的分支：git branch source
- 切换到新分支：git checkout srouce

数据提交到github

```
git add .
git commit -m 'blog 源码'
git push
```

新电脑同步

安装好git， nodejs,  hexo

```
git clone git@github.com:name/name.github.io.git -b srouce blog
# -b 下载指定branch
# blog 本地clone保存文件夹名字
```

