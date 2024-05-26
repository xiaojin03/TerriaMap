# Terria Map

核心功能库修改为使用自己[二次开发的 terriajs](https://github.com/xiaojin03/terriajs)

环境要求：

- The Bash command shell. 如果是 macOS 或 Linux 系统，应该已经自带了。而 Windows 系统则要安装 Git for Windows 获得。
- Node.js v16.0
- npm v8.0
- yarn v1.19.0

## 构建和运行项目

### 一、下载依赖项

```
yarn install
```

因为核心功能库 terriajs 修改为从 github 上下载，而不是在 npm 仓库中下载，下载完依赖项后会有冲突，需要对依赖项中的 terriajs 文件夹进行一些修改。

```
TerriaMap\node_modules\terriajs\node_modules
```

进入以上路径位置，将`.bin`和`d3-color`文件保留，其他都删除掉。

### 二、构建项目

```
yarn gulp
```

对项目代码进行修改后，需要重新运行此命令进行构建，才能生效。

### 三、启动项目

```
yarn start
```

### 四、开发时的热更新启动

```
yarn hot
```
