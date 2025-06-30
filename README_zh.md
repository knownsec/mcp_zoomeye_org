# 🚀 ZoomEye MCP 服务器

一个模型上下文协议（Model Context Protocol，MCP）服务器，基于查询条件提供网络资产信息。该服务器允许大型语言模型（LLMs）通过使用 ZoomEye 的 dorks 和其他搜索参数来获取网络资产信息。

## 🔔 公告

🎉 我们很高兴宣布 **ZoomEye MCP 服务器** 正式开源 — 这是一个强大的模型上下文协议（MCP）服务器，为 AI 助手和开发环境提供实时网络资产情报。

 

🔍 搜索全球互联网资产，追踪实时变化，解锁 AI 驱动的洞察 — 一站式服务。

👉 如何申请：

1. 在 Twitter 上关注我们：[@zoomeye_team](https://x.com/zoomeye_team)
2. 私信我们 "MCP" 和您的 MCP 设置截图
3. 立即获得 7 天会员资格

🎁 限时免费试用 — 立即探索 AI 资产搜索的强大功能！

💡 提供被官方采纳的有见地的反馈，您将解锁**更多奖励**！

🔧 完全兼容领先的 MCP 环境：

- Claude Desktop
- Cursor
- Windsurf
- Cline
- Continue
- Zed
- Cherry Studio
- Chatbox

🔗 在以下平台探索 ZoomEye MCP 服务器：

- GitHub: [knownsec/mcp_zoomeye_org](https://github.com/knownsec/mcp_zoomeye_org)
- MCP.so: [mcp.so/server/mcp_zoomeye](https://mcp.so/server/mcp_zoomeye/zoomeye-ai)
- Smithery: [smithery.ai/server/@zoomeye-ai/mcp_zoomeye](https://smithery.ai/server/@zoomeye-ai/mcp_zoomeye)
- Cursor Directory: [cursor.directory/mcp/zoomeye](https://cursor.directory/mcp/zoomeye)
- Pulse MCP: [pulsemcp.com/servers/zoomeye](https://www.pulsemcp.com/servers/zoomeye)
- Glama MCP: [glama.ai/mcp/servers](https://glama.ai/mcp/servers)

我们欢迎所有人使用、探索和贡献！

## 🔑 如何获取 ZoomEye API 密钥？

要使用此 MCP 服务器，您需要一个 ZoomEye API 密钥。

1. 访问 https://www.zoomeye.org
2. 注册或登录
3. 点击您的头像 → **个人资料**
4. 复制您的 **API-KEY**
5. 设置环境变量：
   
   `export ZOOMEYE_API_KEY="your_api_key_here"`

![zoomeye1](./zoomeye1.png)

![zoomeye2](./zoomeye2.png)

## 功能特点

- 使用 dorks 查询 ZoomEye 获取网络资产信息
- 缓存机制提高性能并减少 API 调用
- 自动重试机制处理失败的 API 请求
- 全面的错误处理和日志记录

## 可用工具

- `zoomeye_search` - 基于查询条件获取网络资产信息。
  - 必需参数：
    - `qbase64` (字符串)：Base64 编码的 ZoomEye 搜索查询字符串
  - 可选参数：
    - `page` (整数)：查看资产页码，默认为 1
    - `pagesize` (整数)：每页记录数，默认为 10，最大为 1000
    - `fields` (字符串)：要返回的字段，用逗号分隔
    - `sub_type` (字符串)：数据类型，支持 v4、v6 和 web。默认为 v4
    - `facets` (字符串)：统计项目，如有多个则用逗号分隔
    - `ignore_cache` (布尔值)：是否忽略缓存