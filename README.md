# openclaw-skills

一组用于在不同平台上自动安装与配置 [OpenClaw](https://github.com/openclaw/openclaw) 的 Claude Code 插件技能集。

## 支持矩阵

### 平台安装

| 平台 | 架构 | 状态 |
|------|------|------|
| macOS | Intel (x86_64) | Coming Soon |
| macOS | Apple Silicon (ARM64) | Coming Soon |
| Windows | WSL2 | Coming Soon |

### 通讯软件集成

| 通讯软件 | macOS | Windows |
|----------|-------|---------|
| 企业微信 | Coming Soon | Coming Soon |
| 钉钉 | Coming Soon | Coming Soon |
| 飞书 | Coming Soon | Coming Soon |
| QQ | Coming Soon | Coming Soon |

## 环境要求

- **Node.js** >= 22
- **npm** / pnpm / bun（任选其一）
- Windows 用户需要 **WSL2** 环境

## 使用方法

### 1. 添加 Marketplace

在 Claude Code 中执行：

```
/plugin marketplace add your-username/openclaw-skills
```

### 2. 查看可用插件

```
/plugin
```

### 3. 安装插件

```
# macOS 用户
/plugin install openclaw-macos

# Windows 用户
/plugin install openclaw-windows
```

安装后，Claude Code 将获得对应平台的 OpenClaw 安装与配置能力。

## 目录结构

```
openclaw-skills/
├── .claude-plugin/
│   └── marketplace.json              # Marketplace 注册配置
├── plugins/
│   ├── openclaw-macos/               # macOS 平台
│   │   └── skills/
│   │       ├── setup/                # 基础安装与配置
│   │       ├── wecom/                # 企业微信集成
│   │       ├── dingtalk/             # 钉钉集成
│   │       ├── feishu/               # 飞书集成
│   │       └── qq/                   # QQ 集成
│   └── openclaw-windows/             # Windows 平台
│       └── skills/
│           ├── setup/                # 基础安装与配置 (WSL2)
│           ├── wecom/                # 企业微信集成
│           ├── dingtalk/             # 钉钉集成
│           ├── feishu/               # 飞书集成
│           └── qq/                   # QQ 集成
└── README.md
```

## 贡献

欢迎提交 PR 或 Issue。如果你有新的平台支持或通讯软件集成需求，请在 Issue 中描述。

## License

MIT
