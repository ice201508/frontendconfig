# frontendconfig
前端常见的一些配置文件

> .npmrc  .gitconfig  .vuerc .eslintrc  .prettietter
> window 开发常见的一些配置


```
1. WIN+R，输入regedit，展开HKEY_CLASSES_ROOT——Directory——Background——Shell——cmd——command，可以看到数据的值应该就是CMD的快捷方式了
2. 右键-- 新建字符串值 --- Icon -- 值就是一个地址c:\windows\xx.ico
```



```
Sublime Text 3 应用技巧和诀窍
http://www.sublimetextcn.com/
```





### .eslintrc

```
配置可以放在 .eslintrc.js 文件里面，  可以放在package.json配置文件里面的eslintConfig字段里

module.exports = {
   root: true,
   env: {
      node: true,
   },
   extends: ['plugin:vue/essential', '@vue/airbnb'],
   parserOptions: {
      parser: 'babel-eslint',
   },
   rules: {
      'no-console': process.env.NODE_ENV === 'production' ? 'error' : 'off',
      'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',
      'vue/no-unused-components': 0,
      'no-unused-vars': 0,
      indent: ['error', 2],
   },
};
```

```
eslint 扩展的一些配置
eslint-config-airbnb  包含了react相关的eslint规则
eslint-config-airbnb-base
eslint-config-standard
eslint-config-alloy  腾讯的eslint规则
可以针对自己的公司人员自己配置一套

插件
eslint-plugin-import
eslint-plugin-vue

https://alloyteam.github.io/eslint-config-alloy/?rule=vue
解释node_modules 里面的 文件查找状态，
```

```
extends: ['plugin:vue/essential', '@vue/airbnb'],
extends: ["eslint-config-alloy/vue"]

比如说 再new Promise里面 不要使用异步async函数，导致失败无法捕捉
回调函数推荐使用箭头函数
函数传递的形参不推荐修改，可以声明一个变量，赋值后再修改
```



### Prettier

```
武断的代码格式化插件，不管语法
.prettierrc 文件  prettier.config.js文件   package.json文件中的prettier字段

module.exports = {
  // 一行最多 100 字符
  printWidth: 100,
  // 不使用缩进符，而使用空格
  useTabs: false,
  // 使用 2 个空格缩进
  tabWidth: 2,
  tabSize: 2,
  // 行尾需要有分号
  semi: true
};
```



### .npmrc

```
https://segmentfault.com/a/1190000015095402
```

