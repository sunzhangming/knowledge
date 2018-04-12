
# git练习
> * [参考地址](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)
### 初始化仓库
`git init`
### 1.添加文件到仓库
* `git add <file>` 
   > 可反复多次使用，添加多个文件
* `git commit -m "解释说明"`
   >提交到仓库
### 2.本地与远程服务器交互
* `git remote add origin git@github.com:sunzhangming/kaoweitong_spider.git`
   > 关联一个远程库
* `git push -u origin master`
   > 第一次推送master分支的所有内容
* `git push origin master`
   > 此后，每次本地提交后
* `git clone git@github.com:sunzhangming/kaoweitong_spider.git`
   > 将服务端代码下载到本地