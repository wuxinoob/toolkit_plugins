# Toolkit Plugins

Toolkit 桌面工具箱官方与社区插件仓库集合。

## 目录结构规划

```
toolkit_plugins/
├── plugins/              # 各独立插件源码目录
│   ├── devtool/          # Windows 开发助手（端口管理、文件锁排查、Hosts/DNS、句柄分析等）
│   ├── eyecare/          # 护眼助手（悬浮胶囊、全屏休息遮罩、键鼠空闲检测）
│   └── moment-notes/     # 拾光便签（WebDAV 同步高颜值便签）
├── docs/                 # 插件开发规范与接口说明
└── README.md
```

## 插件开发规范

每个 Toolkit 插件为一个独立的目录，核心文件包括：
- `plugin.json`：插件元数据清单（ID、名称、版本、视图插槽、权限声明等）
- `main.js`：插件前端 ESM 单文件入口
- 可选的 Sidecar 原生可执行文件（如 Rust / C 编写的辅助进程）
