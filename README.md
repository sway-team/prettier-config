# @swayjs/prettier-config

通用的 prettier 配置。

## 使用

安装 `@swayjs/prettier-config` 为开发依赖：

```bash
npm install @swayjs/prettier-config -D
```

在 `package.json` 中添加以下配置：

```json
{
  "prettier": "@swayjs/prettier-config"
}
```

如果你不想在 `package.json` 中配置的话，也可以通过在根目录下新建 `.prettierrc` 或 `.prettierrc.json` 文件，内容如下：

```json
"swayjs/prettier-config"
```

以上两种形式并没有提供一种方法来扩展我们的配置，如果我们想要覆盖一些配置，可以通过在根目录下新建 `.prettierrc.js` 文件来实现，它是 CJS 模块的导出，内容如下：

```js
module.exports = {
  ...require('@swayjs/prettier-config'),
  semi: true,
}
```

查看 prettier 的[官方文档](https://prettier.io/docs/en/configuration.html#sharing-configurations)以查看共享配置的更多信息。

## @swayjs/prettier-config 配置项

```json
{
  "printWidth": 100,
  "tabWidth": 2,
  "useTabs": false,
  "semi": false,
  "singleQuote": true,
  "quoteProps": "as-needed",
  "jsxSingleQuote": false,
  "trailingComma": "all",
  "bracketSpacing": true,
  "bracketSameLine": false,
  "arrowParens": "avoid",
  "proseWrap": "never",
  "endOfLine": "auto"
}
```

更多配置内容请参考 prettier [官方文档](https://prettier.io/docs/en/options.html)
