# web Server for Render

## 项目结构

- `appweb5.js`：主程序
- `package.json`：Node.js 项目定义，用于 Render 识别

## 部署步骤（简要）

1. 上传整个项目到 GitHub 或直接压缩后上传到 Render
2. Render Web Service 设置：
   - Build Command: `npm install`
   - Start Command: `npm start`
3. 添加环境变量：
   - UUID, SUB_PATH, XPATH, DOMAIN, NAME, PORT（Render 会自动设置 PORT）
4. 完成后访问 `/sub` 获取 web 链接

## 注意事项

Render 平台不允许绑定固定端口，请确保代码使用了：

```js
const PORT = process.env.PORT || ;
```

Render 会自动提供 `PORT` 环境变量。

