# doddle-snippet README

This is the first vscode extension of my own snippets;

## 建一个插件的步骤

### 添加全局库

全局安装
 - vsce: vscode extension build and publish
 - yo: vscode yoman 模板
 - generator-code： yoman相关的吧

```sh
npm i -g yo generator-code vsce
```
### 添加插件代码

### 修改package.json
 - name： 插件名
 - engines： 依赖的vscode版本，与npm包依赖版本规则一致
 - publisher： 发布者id，很重要，与在https://dev.azure.com/closertb/注册的id一致
 - contributes： 关联代码配置

### 添加publisher，
首先，和发布npm包一样，你需要去注册一个发布者账号：https://dev.azure.com/；
接着，就是一些类似于npm login之类的操作了，见：[官方发布流程](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)

```sh
 vsce create-publisher (publisher name) // 添加发布者
 vsce package // 本地打包
 vsce publish // 打包发布
```

package 与 publish并非关联，package主要作用是本地打包，本地安装运行。publish是线上发布用，后台打包并上传发布  


**Enjoy!**
