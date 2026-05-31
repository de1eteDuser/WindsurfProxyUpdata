CURRENT_VERSION=0.1.2

# WindsurfProxy

> **重要声明：本程序仅用于让你在 Windsurf IDE 中使用自定义的第三方 API 中转服务。它不能让你免费使用 Windsurf，也不提供任何 API 额度。你需要自己拥有兼容的 API 中转站（如 OpenAI / Anthropic 兼容的第三方服务）。**

## 这是什么

WindsurfProxy 是一个本地桌面工具，运行在你的电脑上，作为 Windsurf IDE 和你自己的 API 网关之间的中间层。它拦截 Windsurf 的 AI 请求，将其转发到你配置的第三方中转地址，从而让你可以自由选择模型提供商。

## 功能

- **自定义 API 中转** — 将 Windsurf 的 Chat、补全、Embeddings、Web Search 请求路由到你自己的 API 网关
- **多模型支持** — 支持 OpenAI 兼容格式和 Anthropic 兼容格式的中转站
- **跳过连接验证** — 可选跳过 Windsurf 启动时的服务器连接检查，加速启动
- **Windsurf 多开管理** — 支持同时运行多个 Windsurf 实例（分身），每个实例独立管理
- **桌面控制面板** — 提供配置界面、运行状态监控、实时日志查看
- **自动补丁** — 一键应用/恢复 Windsurf 的代理补丁
- **便携版** — 单文件 `.exe`，无需安装，开箱即用
- **自动更新** — 启动时自动检查新版本

## 使用前提

1. 你需要有一个**兼容 OpenAI 或 Anthropic API 格式的中转服务**
2. 你需要有该中转服务的 **API Key**
3. 你需要已安装 **Windsurf IDE**

## 下载

从 [Releases](https://github.com/de1eteDuser/WindsurfProxyUpdata/releases) 页面下载最新的 `WindsurfProxy-x.x.x-win-x64.exe`。

## 快速开始

1. 下载并运行 `WindsurfProxy-x.x.x-win-x64.exe`
2. 在设置页面填入你的中转站地址和 API Key
3. 选择默认模型
4. 点击「应用补丁」让 Windsurf 流量经过本地代理
5. 启动 Windsurf，正常使用 AI 功能

## 配置项

| 配置 | 说明 |
|------|------|
| API Host | 你的中转站地址（OpenAI 或 Anthropic 兼容） |
| API Key | 中转站提供的密钥 |
| 默认模型 | 使用的模型名称 |
| Max Tokens | 最大输出 token 数 |
| 跳过连接验证 | 启动时不等待 Codeium 服务器响应 |
| 允许 MCP 工具 | 是否允许 Windsurf 使用 MCP 工具调用 |

## 常见问题

**Q: 这个工具能让我免费用 Windsurf 的 AI 吗？**

A: 不能。你需要自己有 API 中转服务和对应的 Key。本工具只是把 Windsurf 的请求转发到你指定的地址。

**Q: 支持哪些中转站？**

A: 任何兼容 OpenAI Chat Completions API (`/v1/chat/completions`) 或 Anthropic Messages API (`/v1/messages`) 的服务均可。

**Q: 支持什么系统？**

A: 当前仅支持 Windows x64。

## 免责声明

- 本项目仅供学习研究使用
- 本项目不提供任何 API 服务或额度
- 使用者需自行承担使用风险，并遵守相关服务条款
- 本项目与 Windsurf / Codeium 官方无任何关联
