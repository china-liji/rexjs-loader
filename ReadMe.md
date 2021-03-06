### Rexjs-loader - 是 webpack 利用 Rexjs 打包 es6 语法时，所依赖的 loader。

------

#### 安装、下载
* npm
```
npm install rexjs-loader
```

* Git
```
git clone https://github.com/china-liji/Rexjs-loader.git
```

* Git 仓库

[https://github.com/china-liji/Rexjs-loader](https://github.com/china-liji/Rexjs-loader)

------

#### 快速使用：
于 `webpack.config.js` 中的使用示例：
``` js
module.exports = {
	entry: [
		"./a.js"
	],
	output: {
		path: __dirname,
		filename: "a.min.js"
	},
	module: {
		// 方式1：loaders
		loaders: [
			require("rexjs-loader").getConfig({
				// 可指定模块的根目录，即 import "/xx.js" 相对的根目录
				root: __dirname,
				/*
					* 是否不需要合并 rex-browser-helper.min.js 文件，
					* 一般使用于 rexjs 解析 es6 的环境中，
					* 因为 rex.min.js 已经包括了 rex-browser-helper.min.js 文件。
					*/
				unhelper: false
			})
		],
		// 方式2：rules
		rules: [
			require("rexjs-loader").getRule({
				root: __dirname,
				unhelper: false
			}
		)]
	}
};
```
------
#### Rexjs 仓库地址：
[https://github.com/china-liji/Rexjs](https://github.com/china-liji/Rexjs)

#### Rexjs 官方网站：
[http://www.rexjs.org](http://www.rexjs.org)

#### Rexjs 快速使用：
[http://rexjs.org/#!/book/start/index.md](http://rexjs.org/#!/book/start/index.md)

#### 纯中国制造：
此解析器未引用任何第三方**插件**及**类库**，属于完全独立、创新的一款 ```JavaScript``` 语法编译器，它是 100% **纯中国制造**！