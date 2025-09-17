# 海运清关前端原型运行指南

该仓库目前只包含一个基于 React 的前端原型页面，位于 `frontend/index.html`。要在本地查看或测试该页面，可以按以下步骤操作：

## 先决条件
- 本机需安装 [Node.js](https://nodejs.org/) 或 Python（任选其一，用于启动静态服务器）。
- 现代浏览器（推荐使用 Chrome、Edge 或 Firefox）。

## 使用 Node.js 启动
1. 打开终端，进入仓库目录：
   ```bash
   cd /path/to/phpdomainobject
   ```
2. 进入前端目录并使用 `npx serve`（Node.js 自带的 npx 可直接运行）：
   ```bash
   cd frontend
   npx serve -l 3000
   ```
3. 浏览器访问 `http://localhost:3000` 即可查看原型页面。

## 使用 Python 启动
如果没有 Node.js，也可以使用 Python 内置的简单 HTTP 服务器：

```bash
cd /path/to/phpdomainobject/frontend
python3 -m http.server 3000
```

然后在浏览器访问 `http://localhost:3000`。

> 直接双击 `index.html` 也能打开页面，但部分浏览器在 `file://` 协议下会限制模块脚本。使用本地服务器可以避免这类限制。

## 常见问题
- **页面空白或加载失败**：请确认终端中服务器正在运行，并检查网络是否能访问 CDN（页面依赖公开的 React/Ant Design 资源）。
- **端口被占用**：将命令中的 `3000` 换成其他未占用端口即可，例如 `5000`。

完成测试后，在终端按 `Ctrl + C` 可停止服务器。
