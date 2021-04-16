## 开发说明

### 调试

1. 把 `package.json` 文件中的 `"main": "lib/index.css"` 改成 `"main": "src/index.scss"`

2. 在项目根目录执行以下命令

```
npm link
```

- 该命令会在系统的全局 `npm` 包管理环境中增加当前包的软件链接，使其他项目工程可以通过该软链接直接调用当前包
- 通过软链接建立的包内容的修改可以被监听到，可以触发引用工程的重新构建

3. 在 `hd-theme` 工程根目录执行以下命令

```
npm link @hd-fe/element-theme-chalk
```

- 该命令会把当前工程中 `node_modules` 目录下的相同包名的内容替换为系统的全局 `npm` 包管理环境中相同软链接名指向的内容
