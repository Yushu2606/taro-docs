---
title: OpenEmbeddedAtomicservice
sidebar_label: OpenEmbeddedAtomicservice
---

当元服务需要打开另一个元服务让用户进行快捷操作时，可使用该组件将要打开的元服务以半屏形式跳转。

支持情况：<img title="ASCF元服务" src={require('@site/static/img/platform/ascf.png').default} className="icon_platform" width="25px"/>

> [参考文档](https://developer.huawei.com/consumer/cn/doc/atomic-ascf/components-open-embedded-atomicservice)

## 类型

```tsx
ComponentType<OpenEmbeddedAtomicserviceProps>
```

## 示例代码

```tsx
class App extends Component {
  render () {
    return (
      <OpenEmbeddedAtomicservice
        appid=''
        path=''
        wantParam={{}}
        onTerminated={() => console.log('OpenEmbeddedAtomicservice onTerminated')}
        onError={() => console.log('OpenEmbeddedAtomicservice onError')}
      >
        <Button>Click to open embedded atomicservice</Button>
      </OpenEmbeddedAtomicservice>
    )
  }
}
```

## OpenEmbeddedAtomicserviceProps

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | :---: | --- |
| appid | `string` | 是 | 需要半屏跳转的元服务的AppId参数 |
| path | `string` | 否 | 打开的页面路径。路径后可以带参数，参数与路径之间用?分隔，参数与键值用=相连，多个参数用&分隔。在元服务的App.onLaunch、App.onShow和Page.onLoad的回调函数中可以获得参数query |
| wantParam | `object` | 否 | 需要传递给目标元服务的数据 |
| onTerminated | `CommonEventFunction` | 否 | 退出的回调事件。被半屏打开的元服务正常退出时触发 |
| onError | `CommonEventFunction<OpenEmbeddedAtomicserviceProps.onErrorEventDetail>` | 否 | 异常的回调事件。被半屏打开的元服务发生运行时异常时触发 |

### API 支持度

| API | ASCF元服务 | H5 | React Native | Harmony |
| :---: | :---: | :---: | :---: | :---: |
| OpenEmbeddedAtomicserviceProps.appid | ✔️ |  |  |  |
| OpenEmbeddedAtomicserviceProps.path | ✔️ |  |  |  |
| OpenEmbeddedAtomicserviceProps.wantParam | ✔️ |  |  |  |
| OpenEmbeddedAtomicserviceProps.onTerminated | ✔️ |  |  |  |
| OpenEmbeddedAtomicserviceProps.onError | ✔️ |  |  |  |
