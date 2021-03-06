# tpl-vue-app

Vue App 初始化模板

## 使用

```cmd
yarn install
yarn run serve [APP_ENV]
yarn run build [APP_ENV]
```

## 全局变量

```ts
declare const APP_ENV: string;
declare const APP_MODE: "development" | "production";
```

通常项目开发时可能涉及到多个环境，如 本地、测试、正式 等，额外提供 `APP_ENV` 作为命令行参数注入项目全局

## 项目目录

```code
assets/             静态资源文件
comps/              基础功能组件
views/              模块功能组件
pages/              页面展示组件
plugins/            全局插件
directives/         全局指令
router/             路由配置
store/              数据仓库
style/              全局样式
- index.sass
- normalize.scss    全局样式重置
- heplers.sass      助手类名定义
- _color.sass       色彩变量定义
- _variables.sass   其他变量定义
- _mixins.sass      通用混入定义
utils/
App.vue             项目入口组件
main.ts             项目入口文件
shims-tsx.d.ts
shims-vue.d.ts
```

## 路径别名

```code
'@':         'src'
'@css/vars': 'src/style/_variables.sass'
'@css/mixs': 'src/style/_mixins.sass'
```

## 默认配置

默认支持 pug、sass、ts 语法扩展 <br>
默认引入 vue、vue-router、vuex、axios
默认引入 vue-class-component

## 样式定义

默认引入 style/index.sass 文件

- 使用 [colors.css](http://clrs.cc/) 作为基础色彩变量
- 使用 [open-color](https://yeun.github.io/open-color/) 作为主要色彩变量
- 引入 [normalize](github.com/necolas/normalize.css) 作为样式重置
- index.sass 中添加了部分样式重置
