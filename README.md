# node-utils

## 项目准备

```
npm install
```

- 开发模式运行

```
node app.js  
```

## 使用方式

1、运行

2、将用户提供的模拟数据的D列全选粘到txt中，客户提供数据的最后一行不完整，需要手动处理成json字符串格式

### txt-->xlsx

调用接口：GET   http://localhost:3054/txtToXlsx

参数：

| 参数名     | 示例值                                                       |
| ---------- | ------------------------------------------------------------ |
| inputPath  | D:\测试程序\A320客户提供原始数据.txt (后缀需要是.txt) |
| outputPath | D:\测试程序\A320.xlsx          |

调用完上面的接口后得到了一个xlsx，可以处理参数数据，处理完成后调用下面的接口

### xlsx-->txt

调用接口：GET http://localhost:3054/xlsxToTxt

参数：

| 参数名     | 示例值                 |
| ---------- |---------------------|
| inputPath  | D:\测试程序\A320.xlsx   |
| outputPath | D:\测试程序\A320处理后.txt |

执行完成后将 A320处理后.txt 全选替换到模拟数据D列
