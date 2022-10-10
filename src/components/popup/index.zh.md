---
toc: content
---

# Popup 弹出层

从屏幕滑出或弹出一块自定义内容区。

## 何时使用

适用于展示弹窗、信息提示、选择输入、切换等内容，支持多个弹出层叠加展示。

## 与`antd-mobile`的差异

基于`Mask`实现,差异情况详见`Mask`组件

由于`@react-spring/web`动画不能复用，暂时使用`transition`实现动画，少了一点优雅

## Popup

### 示例

<code src="./demos/demo1.tsx"></code>

<code src="./demos/demo2.tsx"></code>

### 属性

| 属性             | 说明                                                                        | 类型                                                               | 默认值                |
| ---------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------ | --------------------- |
| afterClose       | 完全关闭后触发                                                              | `() => void`                                                       | -                     |
| afterShow        | 完全展示后触发                                                              | `() => void`                                                       | -                     |
| bodyClassName    | 内容区域类名                                                                | `string`                                                           | -                     |
| bodyStyle        | 内容区域样式                                                                | `React.CSSProperties`                                              | -                     |
| className        | 容器类名                                                                    | `string`                                                           | -                     |
| closeOnMaskClick | 点击背景蒙层后是否关闭                                                      | `boolean`                                                          | `false`               |
| destroyOnClose   | 不可见时卸载内容                                                            | `boolean`                                                          | `false`               |
| forceRender      | 强制渲染内容                                                                | `boolean`                                                          | `false`               |
| getContainer     | 指定挂载的 `HTML` 节点，默认为 `body`，如果为 `null` 的话，会渲染到当前节点 | `HTMLElement \| () => HTMLElement \| null`                         | `() => document.body` |
| mask             | 是否展示蒙层                                                                | `boolean`                                                          | `true`                |
| maskClassName    | 遮罩类名                                                                    | `string`                                                           | -                     |
| maskStyle        | 遮罩样式                                                                    | `React.CSSProperties`                                              | -                     |
| onClick          | 点击时触发，常用于阻止事件冒泡                                              | `(event: React.MouseEvent<HTMLDivElement, MouseEvent>) => void`    | -                     |
| onClose          | 关闭时触发                                                                  | `() => void`                                                       | -                     |
| onMaskClick      | 点击蒙层触发                                                                | `(event: React.MouseEvent<HTMLButtonElement, MouseEvent>) => void` | -                     |
| position         | 指定弹出的位置                                                              | `'bottom' \| 'top' \| 'left' \| 'right'`                           | `'bottom'`            |
| showCloseButton  | 是否显示关闭按钮                                                            | `boolean`                                                          | `false`               |
| stopPropagation  | 阻止某些事件的冒泡                                                          | `PropagationEvent[]`                                               | `['click']`           |
| style            | 容器样式                                                                    | `React.CSSProperties`                                              | -                     |
| visible          | 是否可见                                                                    | `boolean`                                                          | `false`               |

### CSS 变量

| 属性      | 说明             | 默认值 | 全局变量          |
| --------- | ---------------- | ------ | ----------------- |
| --z-index | 元素的 `z-index` | `1000` | `--popup-z-index` |
