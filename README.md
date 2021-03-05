# 火币行情插件

## 本地运行

```shell
  npm install
  npm run dev
```

- 生成dist目录后
- 打开chrome浏览器，地址栏输入```chrome://extensions/```，回车。
- 右上角启用```开发者模式```
- 加载已解压的扩展程序
- 选择生成的dist目录文件夹


## 发布版本

> [文档说明](https://vue-web-extension.netlify.app/intro/production-workflow.html#handle-extension-version)

- 使用npm脚本更新版本号，打包的时候会```manifest.json```文件自动使用```package.json```里的版本号

```shell
npm version major # 1.x.x -> 2.x.x, when you release a breaking change
npm version minor # x.1.x -> x.2.x, when you release a feature
npm version patch # x.x.1 -> x.x.2, when you release a patch
npm version 1.2.3 # custom version
```

- ```npm run build```

- 根目录下会生成一个```artifacts```文件夹，里面打包出来zip可用作发布

## 项目模板

> [vue-web-extension](https://vue-web-extension.netlify.app/)

## 过滤控制台无用日志
> 使用了独立vue-devtools后会在控制台输出很多类似```[flush] serialized 206 instances, took 0.9900000004563481ms..```的无用调试日志

- 在控制台 - Console - Filter输入框里输入```-shared -flush```
- 参考：[https://github.com/vuejs/vue-devtools/issues/1151](https://github.com/vuejs/vue-devtools/issues/1151)


