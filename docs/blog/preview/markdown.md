---
title: Markdown 语法与扩展示例
tags:
  - markdown
createTime: 2025/10/11 02:35:31
permalink: /blog/qln10k86/
---

## 标题示例

### 三级标题

#### 四级标题

正文内容演示。

**加粗**、_斜体_、~~删除线~~、==高亮==

数学公式：$E=mc^2$

脚注示例[^1]

---

## 列表与任务

- 无序项一
- 无序项二

1. 有序项一
2. 有序项二

- [x] 已完成
- [ ] 未完成

---

## 表格

| 名称   | 类型   | 备注     |
| ------ | ------ | -------- |
| A      | int    | $100$    |
| B      | string | $abc$    |

---

## 引用与链接

> 这是引用内容。

[内部链接](/)
[外部链接](https://github.com/)

---

## 图片

![Logo](/plume.svg)

---

## Badge 与图标

- <Badge type="info" text="信息" />
- <Badge type="tip" text="提示" />
- <Icon name="material-symbols:home" size="1em" />

---

## 代码块

```js
const a = 1
const b = 2
const c = a + b
```

```ts
function sum(a: number, b: number): number {
  return a + b
}
```

---

## 代码高亮与聚焦

```ts
function foo() {
  const a = 1 // [!code highlight]
  // ...existing code...
}
```

---

## 代码分组

::: code-tabs
@tab JS

```js
console.log('JS 示例')
```

@tab TS

```ts
console.log('TS 示例')
```

:::

---

## 提示块

::: tip
这是一个提示块。
:::

::: warning
这是一个警告块。
:::

---

## demo 示例

:::: demo title="简单示例" desc="演示 HTML/CSS/JS"
::: code-tabs
@tab HTML

```html
<div id="demo">Hello Markdown</div>
```

@tab JS

```js
document.getElementById('demo').style.color = 'blue'
```

@tab CSS

```css
#demo { font-weight: bold; }
```

:::
::::

---

## 脚注

脚注示例[^1]。

[^1]: 这是脚注内容。
import { createHighlighter } from 'shiki'

const highlighter = await createHighlighter({ themes: ['nord'], langs: ['javascript'] })
// @log: Custom log message
const a = 1
// @error: Custom error message
const b = 1
// @warn: Custom warning message
const c = 1
// @annotate: Custom annotation message
```

```ts twoslash
// @errors: 2540
interface Todo {
  title: string
}

const todo: Readonly<Todo> = {
  title: 'Delete inactive users'.toUpperCase(),
//  ^?
}

todo.title = 'Hello'

Number.parseInt('123', 10)
//      ^|

//
//
```

```vue twoslash
<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <p>{{ count }}</p>
</template>
```

**代码分组：**

::: code-tabs
@tab tab1

```js
const a = 1
const b = 2
const c = a + b
```

@tab tab2

```ts
const a: number = 1
const b: number = 2
const c: number = a + b
```

:::

**代码块高亮：**

```ts
function foo() {
  const a = 1 // [!code highlight]

  console.log(a)

  const b = 2 // [!code ++]
  const c = 3 // [!code --]

  console.log(a + b + c) // [!code error]
  console.log(a + b) // [!code warning]
}
```

**代码块聚焦：**

```ts
function foo() {
  const a = 1 // [!code focus]
}
```

::: tip 仅标题
:::

::: note 注释
注释内容 [link](https://github.com/pengzhanbo) `inline code`

```js
const a = 1
const b = 2
const c = a + b
```

:::

::: info 信息
信息内容 [link](https://github.com/pengzhanbo) `inline code`

```js
const a = 1
const b = 2
const c = a + b
```

:::

::: tip 提示
提示内容 [link](https://github.com/pengzhanbo) `inline code`

```js
const a = 1
const b = 2
const c = a + b
```

:::

::: warning 警告
警告内容 [link](https://github.com/pengzhanbo) `inline code`

```js
const a = 1
const b = 2
const c = a + b
```

:::

::: caution 错误
错误内容 [link](https://github.com/pengzhanbo) `inline code`

```js
const a = 1
const b = 2
const c = a + b
```

:::

::: important 重要
重要内容 [link](https://github.com/pengzhanbo) `inline code`

```js
const a = 1
const b = 2
const c = a + b
```

:::

::: details 详细标题

这里是内容。
:::

**GFM alert：**

> [!note]
> note

> [!info]
> info

> [!tip]
> tip

> [!warning]
> warning

> [!caution]
> caution

> [!important]
> important

**代码演示：**

:::: demo title="常规示例" desc="一个常规示例"

::: code-tabs
@tab HTML

```html
<div id="app">
  <h3>vuepress-theme-plume</h3>
</div>
```

@tab Javascript

```js
const a = 'So Awesome!'
const app = document.querySelector('#app')
app.appendChild(window.document.createElement('small')).textContent = a
```

@tab CSS

```css
#app {
  font-size: 2em;
  text-align: center;
}
```

:::
::::

**选项卡：**

::: tabs
@tab 标题1
内容区块

@tab 标题2
内容区块
:::

:::: warning
::: tabs
@tab 标题1
内容区块

@tab 标题2
内容区块
:::
::::

**脚注：**

脚注 1 链接[^first]。

脚注 2 链接[^second]。

行内的脚注^[行内脚注文本] 定义。

重复的页脚定义[^second]。

[^first]: 脚注 **可以包含特殊标记**

    也可以由多个段落组成

[^second]: 脚注文字。

---

## 天猫服务与信息

### 搜索与频道

- 商品、品牌、店铺搜索
- 频道：天猫、喵鲜生、天猫会员、电器城、天猫超市、医药馆、天猫国际、天猫汽车

### 商品分类

- 女装：T恤、连衣裙、衬衫、雪纺衫、风衣
- 男装：夹克、T恤、休闲裤、牛仔裤
- 数码：笔记本、小米、平板电脑、单反
- 家居：四件套、沙发、吸顶灯、马桶、电视柜
- 美妆：面膜、护肤套装、口红、香水、洗发水
- 母婴：亲子装、运动鞋、婴儿玩具、奶粉https://baidu.com
- 美食：坚果、零食、点心、茶叶、葡萄酒
- 运动：鱼竿、运动裤、[跑步鞋](https://baidu.com)

### 购物指南

- 免费注册
- 支付宝开通与充值
- 天猫保障、发票保障、售后规则
- 物流时效保障
- 支付方式：快捷支付、信用卡、余额宝、花呗

### 商家服务

- 商家入驻、商家中心
- 天猫规则、平台协议
- 必修课、喵言喵语

### 关于天猫

- 商家服务大厅、开放平台
- 联系我们、网站合作
- 法律声明、隐私政策、知识产权

### 相关平台

阿里巴巴集团旗下：淘宝、天猫、聚划算、速卖通、1688、阿里妈妈、飞猪、阿里云、AliOS、阿里通信、万网、高德、UC、友盟、钉钉、支付宝、阿里安全

### 法律与备案信息

- 增值电信业务经营许可证：浙B2-20110446
- 出版物网络交易平台备案：新出发浙备字第2024005号
- 营业性演出许可证：浙演经20213300000101
- 集邮市场备案：杭集邮备005
- 互联网违法和不良信息举报：0571-81683755 jubao.tb@service.taobao.com
- 药品、医疗器械、食品等相关资质及备案信息
- © 2003-现在 TMALL.COM 版权所有

pnpm run docs:dev

