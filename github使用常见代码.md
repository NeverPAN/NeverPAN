# git一些常见指令

## 上传指令
git init  
git add README.md  （上传全部文件则git add . ）
git commit -m "first commit"
git branch -M main（有时候是master）
git remote add origin https://github.com/NeverPAN/NeverPAN.git （地址看号）
git push -u origin main
## 拉取指令
git remote add origin https://github.com/NeverPAN/NeverPAN.git
git branch -M main
git push -u origin main

#### 清除url地址：  
git remote -v查看详细信息，显示了两条写错的url地址 解决办法：   
1.使用 git remote rm origin指令移除原先错误的origin remote   
2.使用git remote -v确认已经删除   
3.使用git remote add origin 自己仓库的url地址  

#### 图片插入  
##### 一、插入本地图片   
在 Markdown 中插入本地图片的语法很简单，只需要在文本中添加一个以 ! 开头的行，后面跟着图片的路径。例如：  
![Alt text]（/path/to/image.jpg)   
如果是同文件夹，则直接写图片的名称如1.png，如果是上一文件夹，则写../1.png，以此类推  
在这个例子中，Alt text 是图片的替代文本，当图片无法加载时，将显示这个文本。/path/to/image.jpg 是图片的路径，可以是相对路径或绝对路径。  
##### 二、插入网络图片  
在 Markdown 中插入网络图片也很简单，只需要将图片的 URL 添加到 ![Alt text]（URL) 的语法中即可。例如：  
![Alt text（(https://example.com/image.jpg)    
在这个例子中，Alt text 是图片的替代文本，https://example.com/image.jpg 是图片的 URL。  



#### 更新代码
第一步：查看当前的git仓库状态，可以使用git status  
git status  
第二步：更新全部  
git add *  
第三步：接着输入git commit -m “更新说明”  
git commit -m “更新说明”   
第四步：先git pull,拉取当前分支最新代码（也就是获取GitHub上的最新代码信息，更新本地代码）  
git pull  
第五步：push到远程master分支上（修改本地代码后，再更新GitHub上的代码）  
git push origin master  
不出意外，打开GitHub已经同步了  
总之，先pull，再push  
————————————————  
    版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                       
原文链接：https://blog.csdn.net/jasonLee_lijiaqi/article/details/79947741



#### error: failed to push some refs to的错误，这可能是由于多种原因造成的。
以下是一些常见的解决方案：  
1. 检查远程仓库连接   
确保你的远程仓库连接配置正确。可以使用git remote -v命令查看当前配置的远程仓库。如果配置不正确，可以使用git remote set-url命令重新设置远程仓库地址。  
2. 拉取最新代码  
在推送代码之前，建议先拉取远程仓库的最新代码，确保本地仓库与远程仓库的状态一致。可以使用git pull命令拉取最新代码，并解决潜在的冲突。  
3. 检查分支状态
确保你正在推送的分支是存在的，并且与远程仓库的分支状态一致。可以使用git branch命令查看本地分支，使用git ls-remote --heads命令查看远程分支。  

4. 检查权限问题
确保你有足够的权限将代码推送到远程仓库。如果是私有仓库，可能需要验证身份或获取管理员授权。

5. 使用强制推送
如果以上方法都无法解决问题，可以尝试使用强制推送。使用git push -f命令可以强制将本地仓库的更改推送到远程仓库。但请注意，强制推送会覆盖远程仓库的对应分支，请谨慎使用。

6. 查看错误日志
如果上述方法仍然无法解决问题，可以查看git push命令输出的错误日志，以获取更详细的错误信息。这有助于进一步定位问题所在。

7. 清理缓存
有时，Git的缓存可能会导致推送失败。你可以尝试清理Git的缓存，然后重新推送。可以使用git rm -r --cached .命令清理缓存，然后使用git add .和git commit命令重新提交更改。

总结  
遇到error: failed to push some refs to错误时，不要慌张。按照上述步骤逐一排查问题，相信你一定能够找到解决方案。同时，建议在推送代码之前，先进行充分的测试，确保代码的稳定性和可靠性。


#### Updates were rejected because the tip of your current branch is behind (更新被拒绝，因为当前分支的落后与远程分支)
 
有三种方案：  
push前先将远程repository修改pull下来，然后在推送；  
git pull origin master   
git push -u origin master  
2. 使用强制push的方法：  
git push -u origin master -f   
这样会使远程修改丢失，一般是不可取的，尤其是多人协作开发的时候。  
3. 若不想merge远程和本地修改，可以先创建新的分支:  
git branch [name]   
#然后push   
git push -u origin [name]  

git SSL certificate problem: unable to get local issuer certificate
这个问题是由于没有配置信任的服务器HTTPS验证。默认，cURL被设为不信任任何CAs，就是说，它不信任任何服务器验证。

只需要执行下面命令就可以解决：

git config --global http.sslVerify false
————————————————

  版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/weixin_44014995/article/details/109900149