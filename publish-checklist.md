# Publish Checklist (Public MCP Template)

发布到公共空间前，请逐项确认：

- [ ] 没有任何真实 `Client ID / Client Secret / Token`
- [ ] 没有个人 open_id、邮箱、手机号、回调私域地址
- [ ] 没有你本机绝对路径中暴露隐私目录（可保留通用路径）
- [ ] README 只包含模板步骤，不包含个人账号截图
- [ ] 示例命令中的参数都是占位符
- [ ] 仓库开启 `.gitignore`，避免误提交 `.env` / token 文件

## 推荐额外文件

新增 `.gitignore`：

```gitignore
.env
*.token
*.secret
mcporter.json
```
