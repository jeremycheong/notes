- [git 显示中文乱码](#git-显示中文乱码)
- [git 免密push](#git-免密push)


### git 显示中文乱码
git status查看有改动但未提交的文件时总只显示数字串，显示不出中文文件名，而是显示为八进制的字符编码。    
**解决方案**
```sh
git config --global core.quotepath false
```

### git 免密push
git项目每次提交都要输入密码，不太方便   
**解决方案**    
对项目进行单独的push免密，在项目目录中：    
```sh
git config credential.helper store  
``` 
如果需要设置全局push免密，则需在`config`后加上`--global`参数。