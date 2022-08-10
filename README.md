# @jvbf2e/prettier-config

Quickly format your JavaScript files with this easy to install and use Prettier configuration. This configuration is used on our ESLint React configuration, take a look at [eslint-config](https://github.com/jvbf2e/eslint-config)

## Purpose

[Prettier](https://prettier.io/) is an opinionated code formatter easy to configure and integrate with Code Editors. This configuration aims to quickly install and config JavaScript projects for consistent code style standards.

This package can be used as a stand-alone config or integrated with any linter. If you look to integrate with [ESLint](https://eslint.org/) for React projects take a look at our configuration [eslint-config](https://github.com/jvbf2e/eslint-config) using this Prettier config


## Config

```javascript
module.exports = {
  trailingComma: "es5", // 默认值在 v2.0.0 中从 更改none为es5，"es5":在 ES5 中有效的尾随逗号（对象、数组等）"none"- 没有尾随逗号。"all"- 尽可能使用尾随逗号
  printWidth: 80, // 编辑器展示代码最长距离，超过换行，单位字符。
  tabWidth: 2, // 指定每个缩进级别的空格数。
  useTabs: false, // 使用tab键缩进而不是空格缩进。
  semi: false, // 在语句的末尾打印分号。
  singleQuote: true, // 使用单引号而不是双引号。
  bracketSpacing: true, // 在对象文字中的括号之间打印空格。true- 示例：{ foo: bar }。false- 示例：{foo: bar}。
  bracketSameLine: false, // 多行元素是否能和属性同行（不适用于自闭合元素），默认是 false
  quoteProps: "as-needed", // 对象中的属性使用引号，"as-needed" 只对需要的属性加引号，"consistent" 同一对象中属性引号保持统一，有福同享，有难同当，"preserve" 强制使用引号。默认为 as-needed
  arrowParens: "always", // "always"- 始终包括括号。例子：(x) => x, "avoid"- 尽可能省略括号。例子：x => x
  endOfLine: "lf", // 换行符 "auto" "lf" "crlf"
  requirePragma: false, // 声明格式文件，开启后，仅头部声明的文件进行格式化。用来过度之前没有使用格式化的文件。
  jsxSingleQuote: false, // 在 JSX 中使用单引号而不是双引号。
  jsxBracketSameLine: false, // 在 JSX 中多行元素是否能和属性同行，默认是 false
  embeddedLanguageFormatting: "auto", // "auto"- 如果 Prettier 可以自动识别嵌入代码，请格式化它。"off"- 永远不要自动格式化嵌入代码。
};
```

## How to install

```
npm install prettier @jvbf2e/prettier-config -D
```

## How to use

In your `package.json` add:

```
"prettier": "@jvbf2e/prettier-config"
```

Under script objects

```
"format": "prettier --write \"{,!(node_modules)/**/}*.js\""
```
