# harmony-amap 开发入口

本仓面向 HarmonyOS 7.0.0／API 26，准备高德地图选点、定位、地点查询与地图应用唤起的原生库工程。使用中文交流。

- 先读 [README.md](README.md) 的当前状态与 RN 参考修订。当前仅初始化空 HAR；功能实现须有明确授权，不发布空包。
- Unif 项目约定使用 `unif-harmony-dev`；平台和 HAR 工程分别使用 `uni-harmony-dev`、`uni-harmony-library`。按当前会话实际加载的技能名称取资料，不固定安装缓存路径。
- 目录与文档使用 `uni-code-organization`、`uni-documentation`；按需采用 `unif-architecture-design`、`unif-harmony-test`、`unif-harmony-review` 和 `unif-code-delivery`。CI 机制参考 `uni-github-delivery` 的适用部分。
- 本库尚无鸿蒙公开能力。RN 只作为行为与资源参考，不能改包名后充当原生 API；恢复实现时核对有效契约、当前 RN 源、完整依赖及原生 SDK，不编造专属技能或规范路径。
- 保留实际平台、身份、取消、迟到回调与资源所有权差异。共享源从权威来源更新；新增权限、依赖、外部服务和部署接线不得超出任务范围。
- 基础 CI 只检查工作流语法及 PR 标题。源码、自动化、空 HAR、真实宿主、设备和业务验收分别报告；构建通过不等于功能可用。
- 库改动走独立分支 PR，提交和 PR 标题、正文使用中文。提交、推送、合并、发布按当前授权执行；常规发版只改 minor 或 patch，major 升级须明确授权。
- 保留工作区已有修改；凭据、个人设备信息、本机配置及原始运行产物不入库。安全报告见 [SECURITY.md](SECURITY.md)。
