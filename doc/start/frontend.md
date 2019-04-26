## 1 、代码clone {docsify-ignore}

```bash
git clone git@github.com:YuKongEr/panda-admin.git
```

clone完后，使用vscode打开项目。

## 2、安装依赖{docsify-ignore}

在项目目录打开终端。

如果是win用户 按住`shift`键右键 点击打开命令行即可在当前路径打开命令行.

- npm用户使用 `npm i`即可安装
- yarn用户输入`yarn ` 即可安装

## 3、配置处理  {docsify-ignore}

修改后端接口api地址

文件路径

`panda-admin\config\dev.env.js`

```javascript
module.exports = merge(prodEnv, {
  NODE_ENV: '"development"',
  // 后台api地址 默认是网关地址
  BASE_API: '"http://127.0.0.1:2004"',
})
```



## 4、启动  {docsify-ignore}

在项目目录打开终端。

- npm用户使用 `npm run dev`即可安装
- yarn用户输入`yarn  run dev` 即可安装