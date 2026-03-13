# openclaw-skills

一组用于在不同平台上自动安装与配置 [OpenClaw](https://github.com/openclaw/openclaw) 的 Claude Code 插件技能集。

## 支持矩阵

| 通讯软件 | macOS | Windows |
|----------|-------|---------|
| 企业微信 | ✅ | ✅ |
| 钉钉 | Coming Soon | Coming Soon |
| 飞书 | Coming Soon | Coming Soon |
| QQ | Coming Soon | Coming Soon |

## 环境要求

- **Node.js** >= 22
- **npm**（用于安装 OpenClaw）
- Windows 用户需要 **WSL2** 环境

## 使用方法

### 1. 添加 Marketplace

在 Claude Code 中执行：

```
/plugin marketplace add your-username/openclaw-skills
```

### 2. 安装插件

```
/plugin install openclaw-skills
```

安装后，Claude Code 将获得对应平台的 OpenClaw 安装与配置能力。

### 3. 使用 Skill

安装插件后，可通过 skill 名称触发对应配置流程，例如：

```
/skill macos-wecom
/skill windows-wecom
```

## 可用 Skills

| Skill 名称 | 说明 |
|------------|------|
| `macos-wecom` | macOS 企业微信集成 |
| `macos-dingtalk` | macOS 钉钉集成 |
| `macos-feishu` | macOS 飞书集成 |
| `macos-qq` | macOS QQ 集成 |
| `windows-wecom` | Windows 企业微信集成 |
| `windows-dingtalk` | Windows 钉钉集成 |
| `windows-feishu` | Windows 飞书集成 |
| `windows-qq` | Windows QQ 集成 |

## 目录结构

```
openclaw-skills/
├── .claude-plugin/
│   └── marketplace.json              # Marketplace 注册配置
├── plugins/
│   └── openclaw-skills/
│       └── skills/
│           ├── macos-wecom/          # macOS 企业微信集成
│           ├── macos-dingtalk/       # macOS 钉钉集成
│           ├── macos-feishu/         # macOS 飞书集成
│           ├── macos-qq/             # macOS QQ 集成
│           ├── windows-wecom/        # Windows 企业微信集成
│           ├── windows-dingtalk/     # Windows 钉钉集成
│           ├── windows-feishu/       # Windows 飞书集成
│           └── windows-qq/           # Windows QQ 集成
└── README.md
```

## 贡献

欢迎提交 PR 或 Issue。如果你有新的平台支持或通讯软件集成需求，请在 Issue 中描述。

## License

MIT
