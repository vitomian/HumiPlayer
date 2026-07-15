<div align="center">

<img src="HumiPlayer/Assets/logo.png" alt="HumiPlayer Logo" width="200"/>

# HumiPlayer

**直播场景搭建 & 特效快捷键播放器**

一款面向直播主播的桌面工具 — 搭建带透明区域的直播场景，用快捷键触发自定义特效。

</div>


## 功能特性

### 场景搭建编辑器

多图层可视化编辑器，为直播搭建带透明区域的装饰场景。

- 多类型图层：支持添加图片、GIF、视频、文本图层
- 自由布局：拖拽定位、缩放、网格辅助线
- **挖空操作**：矩形/圆形选区在图片上擦出透明区域，让直播画面从边框"窗户"中透出
- 撤销/重做：最多 10 步历史记录，随时修改不留风险
- 多格式导出：PNG / JPG / BMP / WebP
- 场景全屏播放：透明模式下鼠标可穿透，作为直播覆盖层

### 快捷键特效播放

预设素材，一键触发，用表情包和动图回应观众互动。

- 最多 10 个特效位，每个绑定独立快捷键（支持组合键）
- 支持图片、GIF、短视频（最长 5 秒）
- 全局热键：在任何应用界面下按下都能触发
- 播放窗口置顶弹出，ESC 一键退出

### 其他功能

- 新手引导教程：首次使用自动引导核心操作
- 暗色/亮色主题切换
- 开机自启动
- 自动更新

---

## 解决什么问题

**场景搭建太麻烦？** 以前要在装饰边框上挖透明区域只能用 PS 做蒙版，现在 AI 出图虽然快，但后期处理透明区域对非专业用户来说门槛极高。HumiPlayer 让你直接在工具里画选区就能挖空，改了不满意随时撤销重画。

**直播互动特效没法自定义？** 平台自带的礼物特效和弹幕特效主播无法控制。HumiPlayer 让你预设自己的表情包、动图、短视频，绑上快捷键，直播时按一下就弹出来。

---

## 项目结构

```
01HumiPlayer/
├── HumiPlayer/                  # 主客户端
│   ├── Views/                   # 页面视图
│   │   ├── WelcomeView.axaml          # 欢迎页
│   │   ├── LayerMainView.axaml        # 媒体设置容器
│   │   ├── SceneBuilderView.axaml     # 场景搭建编辑器（核心）
│   │   ├── MagicLibraryView.axaml     # 魔法库入口
│   │   ├── PlayWindow.axaml           # 特效播放窗口
│   │   ├── ScenePlayWindow.axaml       # 场景播放窗口
│   │   └── ...                        # 对话框、素材库等
│   ├── ViewModels/              # ViewModel 层
│   ├── Services/                # 服务层
│   │   ├── ImageProcessingService    # 图片处理与画布渲染
│   │   ├── ExportQuotaService        # 配额管理
│   │   ├── PaymentApiClient          # 支付接口
│   │   ├── UpdateService             # 自动更新
│   │   └── MaterialLibraryService    # 素材库管理
│   ├── Helpers/                  # 工具类
│   │   ├── GlobalHotkeyManager      # 全局热键注册
│   │   ├── AlphaVideoDecoder        # Alpha 通道视频解码
│   │   └── LicenseManager            # 许可证验证
│   └── Assets/                   # 资源文件
├── HumiActivationTool/          # 激活码管理工具
├── HumiServer/                  # 后端服务（ASP.NET Core Minimal API）
├── HumiCloudFunctionPython/     # 云函数
└── HumiPlayer.sln               # 解决方案文件
```

---

## 快速开始
前往 [Releases](https://github.com/your-username/HumiPlayer/releases) 页面下载最新安装包，双击安装即可使用。

### 环境要求

- .NET 8.0 SDK
- Windows 10+ / macOS 10.15+


## 许可证

本项目采用 [MIT License](LICENSE) 开源。

---
