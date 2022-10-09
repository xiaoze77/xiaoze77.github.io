---
toc: content
---

# Popup 弹出层

从屏幕滑出或弹出一块自定义内容区。

## 何时使用

适用于展示弹窗、信息提示、选择输入、切换等内容，支持多个弹出层叠加展示。

## 与`antd-mobile`的差异

由于`Mask`暂时精简实现方式，所以`popup`暂时部支持下列属性

`stopPropagation`

`react-spring`动画不能复用，使用`transition`实现动画

## Popup

### 示例

<code src="./demos/demo1.tsx"></code>

<code src="./demos/demo2.tsx"></code>

### 属性

| 属性           | 说明                                                                        | 类型                                                               | 默认值          |
| -------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------ | --------------- |
| visible        | 是否可见                                                                    | `boolean`                                                          | `false`         |
| onMaskClick    | 点击蒙层触发                                                                | `(event: React.MouseEvent<HTMLButtonElement, MouseEvent>) => void` | -               |
| destroyOnClose | 不可见时卸载内容                                                            | `boolean`                                                          | `false`         |
| forceRender    | 强制渲染内容                                                                | `boolean`                                                          | `false`         |
| getContainer   | 指定挂载的 `HTML` 节点，默认为 `body`，如果为 `null` 的话，会渲染到当前节点 | `HTMLElement \| () => HTMLElement \| null`                         | `document.body` |
| afterClose     | 完全关闭后触发                                                              | `() => void`                                                       | -               |
| position       | 指定弹出的位置                                                              | `'bottom' \| 'top' \| 'left' \| 'right'`                           | `'bottom'`      |
| className      | 容器类名                                                                    | `string`                                                           | -               |
| style          | 容器样式                                                                    | `React.CSSProperties`                                              | -               |
| bodyClassName  | 内容区域类名                                                                | `string`                                                           | -               |
| bodyStyle      | 内容区域样式                                                                | `React.CSSProperties`                                              | -               |
| maskClassName  | 遮罩类名                                                                    | `string`                                                           | -               |
| maskStyle      | 遮罩样式                                                                    | `React.CSSProperties`                                              | -               |
| onClick        | 点击时触发，常用于阻止事件冒泡                                              | `(event: React.MouseEvent<HTMLDivElement, MouseEvent>) => void`    | -               |

### CSS 变量

| 属性      | 说明             | 默认值 | 全局变量          |
| --------- | ---------------- | ------ | ----------------- |
| --z-index | 元素的 `z-index` | `1000` | `--popup-z-index` |
