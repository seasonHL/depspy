# node 层与 view 层间的通信

借助 `WebSocket` 服务，在 `node` 层与 `view` 层间建立通信。

初次启动时，根据配置项初始化 UI 页面。

## 当从 UI 页面改变 depth 时

通过 `ws` 告知 `node` 层，`node` 层重新计算，然后将结果通过 `ws` 传回。

## 当前项目的依赖发生变化时

`node` 层监听 `package.json` 文件中相关信息的变化，当发生变化时，重新计算依赖关系，然后将结果通过 `ws` 传回。