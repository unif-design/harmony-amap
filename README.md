# harmony-amap

面向 HarmonyOS 7.0.0／API 26，为高德地图选点、定位、地点查询与地图应用唤起的原生实现准备工程入口。

当前仅有仓库规范与空 HAR 骨架。根工程只注册 `library`，`library/Index.ts` 为 `export {};`，没有公开 API、业务功能、运行示例或可安装 HAP。`AppScope/` 只提供 SDK 所需工程元数据。

## 打开与构建

使用配套 API 26 SDK 的 DevEco Studio 打开仓库根目录。`targetSdkVersion`、`compatibleSdkVersion` 和 Hvigor `modelVersion` 均为 `26.0.0`。

```sh
devecocli build --modules library --build-mode release
```

输出为 `library/build/default/outputs/default/library.har`。构建只验证工程配置与空 HAR 打包，不能证明功能或设备行为；HAR 本身不能安装到设备。构建产物和本机缓存不入库。

包名为 `@unif/harmony-amap`，`0.0.0` 仅为未发布占位版本。空包不发布；首次正式发行前重新核对 RN 采用版本、OHPM 历史及实际公开能力。

## RN 对照准备

初始化时登记的 RN main 快照为 [`@unif/react-native-amap@0.2.1`](https://github.com/unif-design/react-native-amap/tree/3226d95ddd7ce722abc6fc58a975c63ccb8333db)，修订 `3226d95ddd7ce722abc6fc58a975c63ccb8333db`。该快照提供行为和许可参考，不表示鸿蒙已实现对应功能或已引入 RN 依赖。

恢复实现时重新核对当前有效契约、RN 公开导出、完整依赖与实际消费者，再确定共享源码、原生适配和共同验收案例。RN API、SDK 和 React 接口不能直接作为原生鸿蒙出口。

## 开发与交付

先读 [AGENTS.md](AGENTS.md)。当前范围为初始化，功能开发须另有明确要求；新增依赖、权限、外部服务及发布接线按实际授权处理。

基础 CI 配置工作流语法检查，另有 PR 标题检查；本地运行 `actionlint -no-color`。完整云端 SDK 构建和 OHPM 自动发布尚未接入，配置文件不证明远端 CI 或分支保护已经生效。

源码检查、自动化、HAR 构建、实际宿主消费、设备运行和业务验收分别记录。提交与 PR 使用中文，库改动走分支 PR；发布不由提交类型自动授权。

## 来源与许可

- 工程配置与忽略规则复用已构建的 [API 26 空 HAR 骨架](https://github.com/unif-design/harmony-camera/tree/5a290983ca0d241d2e8e49b70d832242d4b7b688)。
- PR／Issue 与工作流规则依据 [Uni Skills 交付模板](https://github.com/unif-skill/uni-skills/tree/491d2bbc4c4106a1d87de85871e67faf70a856d0/skills/uni-github-delivery/templates) 做原生适配；组织贡献与安全约定见 [组织入口](https://github.com/unif-design/.github/blob/b3d5aaf66c9df38135e9770eb605eb60366df816/README.md)。本仓仅采用平台无关部分，没有接入 RN 专用同步器、`delivery.json` 校验或 npm 发版流程。
- 根目录与 HAR 均采用对应 RN 修订的 MIT 许可，保留原版权声明，见 [LICENSE](LICENSE)。

安全问题按 [SECURITY.md](SECURITY.md) 私密报告。
