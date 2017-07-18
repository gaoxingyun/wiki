# wiki

#### 环境搭建
###### 搭建工具
- wiki工具[https://github.com/gollum/gollum](https://github.com/gollum/gollum)

###### wiki地址
- wiki地址：[http://119.23.43.25:12345](http://119.23.43.25:12345)

###### 同步脚本
- 修改wiki页面的提交每天通过crontab定时push代码到wiki仓库。
``` crontab
0 0 22 * *  /home/wiki/wiki/autopush.sh
```

``` autopush.sh
WIKI_HOME=~/wiki
cd $WIKI_HOME
/usr/bin/git pull
/usr/bin/git push
```
