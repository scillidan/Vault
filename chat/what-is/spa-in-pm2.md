What is `--spa` in PM2?

````md
In PM2, which is a popular process manager for Node.js applications, the `--spa` flag is used to enable Single Page Application (SPA) mode. This is specifically relevant when you are serving static files with PM2, particularly when the application involves client-side routing.

When you use the `--spa` flag, PM2 will configure the server to always return your `index.html` file for any routes that are not found. This is necessary for SPAs because routing is typically handled on the client side (using libraries like React Router, Vue Router, etc.), and any attempt to navigate directly to a deep link should still return the main `index.html` file to allow the client-side router to take over.

Here’s a quick example of how you might use the `--spa` flag with PM2:

```bash
pm2 serve build 3000 --spa
```

In this command:

- `build` refers to the directory containing your built static files (like from a React or Vue application).
- `3000` is the port where the server will listen.
- `--spa` ensures that your single-page application works correctly by handling routing properly.

This setup is useful for web applications that utilize modern JavaScript frameworks for building user interfaces.
````

```md
在 PM2 中，PM2 是一个流行的 Node.js 应用程序进程管理器，`--spa` 标志用于启用单页应用程序（SPA）模式。当您使用 PM2 服务静态文件时，这一点尤其相关，尤其是当应用程序涉及客户端路由时。

当您使用 `--spa` 标志时，PM2 将配置服务器以始终返回您的 `index.html` 文件，用于任何未找到的路由。这对于 SPA 来说是必要的，因为路由通常是在客户端处理的（使用像 React Router、Vue Router 等库），而直接导航到深链接的任何尝试仍应返回主 `index.html` 文件，以便客户端路由器可以接管。

以下是您如何使用 `--spa` 标志与 PM2 的一个简单示例：

```bash
pm2 serve build 3000 --spa
```

在这个命令中：

- `build` 指的是包含您构建的静态文件的目录（例如来自 React 或 Vue 应用程序）。
- `3000` 是服务器将监听的端口。
- `--spa` 确保您的单页应用程序正常工作，通过正确处理路由。

此设置对于利用现代 JavaScript 框架构建用户界面的 Web 应用程序非常有用。
```