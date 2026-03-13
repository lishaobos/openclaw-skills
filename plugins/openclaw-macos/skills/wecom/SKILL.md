---
name: wecom
description: 在 macOS 上安装 OpenClaw 并配置企业微信长连接集成
---

# OpenClaw macOS 企业微信集成

你是一个安装配置助手，帮助用户在 macOS 上安装 OpenClaw 并配置企业微信。

## 第一步：确认 Node.js 环境

运行 `node --version` 检查版本，要求 **Node.js >= 22**。

- 如果未安装或版本不满足，通过 Homebrew 安装：
  ```bash
  brew install node@22
  ```

## 第二步：安装 OpenClaw

先配置国内镜像：
```bash
npm config set registry https://registry.npmmirror.com
```

安装 OpenClaw：
```bash
npm install -g openclaw@latest
```

安装完成后验证：
```bash
openclaw --version
```

## 第三步：配置企业微信频道

编辑 `~/.openclaw/openclaw.json`，需要用户提供以下必填参数：

- **botId**：企业微信 AI 机器人 Bot ID（在企业微信管理后台「应用管理」→「智能机器人」中创建，选择长连接模式后获取）
- **secret**：企业微信 AI 机器人 Secret

配置示例：

```json
{
  "channels": {
    "wecom": {
      "enabled": true,
      "dmPolicy": "open",
      "groupPolicy": "open",
      "botId": "<用户提供的 botId>",
      "secret": "<用户提供的 secret>"
    }
  }
}
```

## 第四步：设置 Gateway 模式

```bash
openclaw config set gateway.mode local
```

## 第五步：配置工具 Profile

在 `~/.openclaw/openclaw.json` 中添加或修改 `tools` 配置，确保 `profile` 值为 `"full"`：

```json
{
  "tools": {
    "profile": "full"
  }
}
```

如果文件中已有 `tools` 配置但 `profile` 值不是 `"full"`，需要修改为上述值。

## 第六步：安装企业微信插件

```bash
openclaw plugins install @sunnoy/wecom
```

## 第七步：重启 Gateway

```bash
openclaw gateway restart
```

## 验证

重启完成后，在企业微信中向机器人发送消息，确认能正常收到回复。

如有问题，运行 `openclaw doctor` 进行诊断。
