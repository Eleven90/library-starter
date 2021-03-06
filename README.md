# [library-starter](https://github.com/eleven-net-cn/library-starter)

Typescript 工具类库快速启动工具

- Babel 编译 TypeScript 代码，tsc 代码检查、生成声明文件等
- Jest 单元测试，使用 ts-jest 转换测试代码、`test` 目录的 Typescript 代码检查
- TypeDoc 自动生成文档
- 保持统一的代码规范，commit 提交时自动格式化代码（eslint、prettier、lint-staged）
- 强制规范 `git commit` 提交（commitlint、commitizen）

## Usage

> 执行以下两步操作，即可快速完成类库工具搭建。

1. `clone`

   ```sh
   # YOUR_PROJECT_FOLDER_NAME 是你的项目目录名
   git clone https://github.com/eleven-net-cn/library-starter.git YOUR_PROJECT_FOLDER_NAME

   cd YOUR_PROJECT_FOLDER_NAME
   ```

2. `install`

   ```sh
   yarn / yarn install
   ```

   > `install` 安装完包以后，会提示输入 library 名称，该 library 名称会被处理成小驼峰变量，作为 UMD 模块挂载到 window、global 的全局变量。  
   > 例如：library 名称为 my-lib，默认情况下，UMD 模块挂载的全局变量是 `window.myLib`、`global.myLib`。

## Command

```sh
yarn start          # 本地调试 & tsc 类型检查（src 目录）
yarn test           # 启动 Jest 测试 & 查看测试覆盖率 & 类型检查（test 目录）
yarn build          # 打包 & 类型检查 & 生成声明文件 & 生成 docs 文档
yarn docs           # 生成文档 By TypeDoc

yarn release            # 根据 commit 提交，自动升级 version、生成 CHANGELOG.md
yarn release:patch      # 自动升级小版本号、生成 CHANGELOG.md
yarn release:minor      # 自动升级次版本号、生成 CHANGELOG.md
yarn release:major      # 自动升级主版本号、生成 CHANGELOG.md

yarn commit         # 交互式书写 commit message
yarn lint           # 运行 eslint，查看 lint 提示
yarn lint:fix       # 运行 eslint & 自动 fix 代码
```
