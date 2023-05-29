# pipreqs
> 为python项目生成reqirements.txt

## 安装
```
pip install pipreqs
```

## 使用
```
cd projectFolder
pipreqs .
```

## 其他生成requirements.txt的方式
pip freeze > requirements.txt

## 删除requirements.txt 后缀文件
正则表达式匹配：
'''
@ file:.*[\d\s\w]*
'''
