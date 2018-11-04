# me_vuedemo

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


作为一个Java后端开发者,小编已经将近3年没有写过前端了,当年在学校学习时候,H5刚出来,
我们都是用纯html标签+bootstrap样式来写网页的，还记得第一个网页写的是小米的官网。
时隔3年后，再次有了一个新的念头,写写前端,刚开始小编想用React来写的，
奈何React不支持双向数据绑定(其实是太难了,学不会^_^),于是就考虑了一个国产的VUE,
听说VUE是很简单,于是我也跃跃欲试。前期断断续续积累支持大概一周时间。学习了基础语法。
感觉还可以。没有React那么难。于是周末11/03就模仿写了一个慕课网的页面，用到的技术是VUE+饿了么的Element。
下面将过程分享出来，并谈谈我对现代前端模块化开发的感受。因为不是专业的前端开发,所以大神勿喷。


### 作品展示慕课网

![](http://p3.pstatp.com/large/pgc-image/302d6405abd5499b8c8d2164802e2a01)



### 技术栈: VUE + ElementUI + axios

- 第一部分: 主要模仿慕课网
- 第二部分: 利用axios网络请求,随机生成诗词,添加todoList


#### 第一部分: 主要模仿慕课网

项目目录(主要分为5个组件)

![](http://p3.pstatp.com/large/pgc-image/d3cb370fd9364c2098b8d11227bcd3ea)

页面分别对应的模块
![](http://p99.pstatp.com/large/pgc-image/cb9f6e73ff1741f994d142b6d7f648de)



#### navMenu.vue

主要包含一个慕课网的login和文本和搜索框。

![](http://p9.pstatp.com/large/pgc-image/1df716d7f45742fb99f6eb220cbfd748)

然后从ElementUI中找到模板，并填充自己的内容。并添加css阴影样式

![](http://p3.pstatp.com/large/pgc-image/c7ed5767171241ff8481625f9ed4c75b)
![](http://p3.pstatp.com/large/pgc-image/ab8b0a627a094de79264bc2c1ca49d03)
添加阴影
![](http://p99.pstatp.com/large/pgc-image/f387cf0db8c143dbbe58b7e2f76dbc8f)

#### bannerCard.vue

![](http://p1.pstatp.com/large/pgc-image/d82da4875db540529bcfd2a7bbce70b9)

到ElementUI找布局
![](http://p3.pstatp.com/large/pgc-image/4ab76c19ec6b425396266961023a3082)

Aside中添加10个按钮(并添加css样式保持背景颜色一样)
![](http://p9.pstatp.com/large/pgc-image/e082f9e638164497aaf563b0821b492d)
Header中添加一个走马灯

![](http://p3.pstatp.com/large/pgc-image/4c1d6d00818e47f3b0e064a3ca6a1bc3)

Main中添加四个(css样式参考慕课网)
![](http://p3.pstatp.com/large/pgc-image/8056197f96924798a799df19812c7d50)
![](http://p1.pstatp.com/large/pgc-image/1c8072f017614a889a2852d2bb6a8073)

#### segmentation.vue
分割符号（前后在模板中添加两个加载转圈的logo并css为红色文本作为变量支持自定义）
![](http://p3.pstatp.com/large/pgc-image/0af9bdc4f2b543b5bc2e6058a09f88bf)

![](http://p3.pstatp.com/large/pgc-image/08f063b868b1447f8553a6c722d8914e)


#### shopClass.vue
原理类似todoList定义个卡片,根据数量来展示

![](http://p99.pstatp.com/large/pgc-image/6da24da682684b37888462ae6d3ff6b9)

到ElementUI中找到卡片组件
![](http://p3.pstatp.com/large/pgc-image/0d6824a87bfe4e869c4799d13c37a7c4)

![](http://p3.pstatp.com/large/pgc-image/1da522f6f4744cba90972dff7a85174a)

#### todoList
另外因为是写的第一个VUE例子,也写了一个todoList的例子,放在页面下方。可以随机生成诗词并添加到todoList中

![](http://p3.pstatp.com/large/pgc-image/50dcdcbd592a4b90b0d0a84123fc8e62)

原理是:

利用axios请求一个诗词API并通过VUE双向绑定展示到input便签中,当添加按钮指定就添加到诗词list中。

下面利用v-for展示todoList

![](http://p3.pstatp.com/large/pgc-image/0ef4834b4f974c3a9c927752ca9386bb)
![](http://p9.pstatp.com/large/pgc-image/00e0bbe750824e7286b7ad7bee13a1ea)

到这里基本所有的内容描述了，如果也要练习建议代码克隆下来,仔细研究。VUE是很简单的，小编总共就学习了不到1周的时间,如果要算总时间应该也不超过24小时。说这些的目的并不是炫耀而是说一个道理,就是编程都是想通的,当你会一门语言，那么在学习其他语言就都是简单的.编程都是面向对象。

总结下来，现代的前端开发已经和之前小编学习时候是今非昔比了,难度不亚于后端开发,不过组件是开发是可以二次利用的,定义好组件，很多地方都可以使用(就像上面的segmentation.vue和shopClass.vue一样)。感兴趣的同学可以来学前端。
