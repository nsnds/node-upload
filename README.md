# node-upload

node框架使用express，安装脚手架工具```npm i express-generator -g```

文件处理中间件使用multer

app.js：
```js
/* 导入upload模块 */
const uploadRouter = require('./routes/upload')

/*  */ 允许跨域访问
app.all('*', function(req, res, next) {  
  res.header("Access-Control-Allow-Origin", "*");  
  res.header("Access-Control-Allow-Headers", "X-Requested-With");  
  res.header("Access-Control-Allow-Methods","PUT,POST,GET,DELETE,OPTIONS");  
  res.header("X-Powered-By",' 3.2.1')  
  res.header("Content-Type", "application/json;charset=utf-8");  
  next();
});

/* 使用upload路由 */
app.use('/upload', uploadRouter);
```

[参考链接](https://blog.csdn.net/kaelyn_X/article/details/78822006)