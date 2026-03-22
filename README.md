# dida-mcp (Public Template)

这是一个可公开分享的 **滴答清单 MCP 接入模板**（空壳）。

- ✅ 已去除所有个人敏感信息
- ✅ 可直接给别人按步骤配置
- ❌ 不包含任何可用凭证/Token

---

## 1) 前置条件

- 已安装 `mcporter`
- 有滴答清单开发者应用（可获取 Client ID / Client Secret）
- 本机可用一个 OAuth 回调地址（例如 `http://localhost:18090/callback`）

---

## 2) 配置文件示例

将 `mcporter.template.json` 复制为你自己的：

```bash
cp mcporter.template.json ~/.mcporter/mcporter.json
```

然后把占位符替换为你自己的值：

- `YOUR_DIDA_CLIENT_ID`
- `YOUR_DIDA_CLIENT_SECRET`
- `YOUR_DIDA_REDIRECT_URI`

---

## 3) 授权

按你的 dida-mcp 实现方式完成 OAuth 授权（拿到你自己的 token）。

> 没有授权，MCP 无法创建/修改任务。

---

## 4) 验证

```bash
mcporter list dida-mcp --schema
mcporter call dida-mcp.get_projects --output json
mcporter call dida-mcp.create_task --args '{"title":"测试任务"}' --output json
```

---

## 5) 安全建议

- 不要把 `Client Secret`、OAuth token、用户数据提交到公开仓库
- 建议把敏感配置放在本地环境变量或私有配置中
- 对外只发布模板（像本仓库这样）

---

## 6) 目录说明

- `mcporter.template.json`：公开模板配置（空壳）
- `publish-checklist.md`：发布前检查清单
