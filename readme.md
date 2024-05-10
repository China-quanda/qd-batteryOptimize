# qd-batteryOptimize 开发文档

## 忽略电池优化的含义
一、忽略电池优化的含义 忽略电池优化是指在安卓系统中的电池优化功能中，用户可以选择忽略某个应用的电池优化。这意味着该应用将在后台继续运行，即使系统认为它在耗费更多的电量。
二、忽略电池优化会有什么影响？ 如果忽略了某个应用的电池优化，那么该应用将继续在后台运行，这可能会对电池寿命和电量消耗产生不良影响。此外，某些应用可能在后台耗费更多的网络数据，从而导致更高的数据费用。

## 功能

- 查询当前应用是否忽略电池优化。
- 请求忽略电池优化设置。

## 安装

请将此插件的代码包括在您的项目中，并确保所有依赖项正确导入。

## 如何使用

### 在 script 中引入

```
import { checkBatteryOptimizeStatus, requestIgnoreBatteryOptimization } from '@/uni_modules/qd-batteryOptimize';
```


### 查询电池优化状态

要查询应用当前是否忽略电池优化，请使用以下方法：

```
checkBatteryOptimizeStatus().then((isIgnoring) => {
    if (isIgnoring) {
        console.log("应用当前忽略电池优化");
    } else {
        console.log("应用当前未忽略电池优化");
    }
});
```

### 请求忽略电池优化

要请求用户允许应用忽略电池优化，请使用以下方法：

```
requestIgnoreBatteryOptimization().then((result) => {
    if (result) {
        console.log("用户允许忽略电池优化");
    } else {
        console.log("用户未允许忽略电池优化");
    }
});
```

## 注意事项

请确保您的应用遵守相关平台的政策和指南，特别是与前台服务和电池优化相关的部分。

## 贡献

欢迎对此插件提出改进建议或提交问题报告。



