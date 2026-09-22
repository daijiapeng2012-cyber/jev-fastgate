# JEV FastGate

JEV FastGate 是一层给 Codex 使用的高速判断门，用来处理路由、分类、评分和验收判断。它把封闭、结构化的问题先变成可回读的判断信号；遇到开放式推理、低置信度或高风险动作时，继续交给 Codex、测试或人工复核。

线上页面：[shuntian.uk/works/jev-fastgate](https://shuntian.uk/works/jev-fastgate/)

## 当前内容

- `index.html`：可直接部署的单文件产品说明页。
- 页面内含安全的 Codex MCP 配置模板，只转发 `TYPESAFE_API_KEY` 环境变量。
- 页面不会保存真实 API Key，也不承担安全边界、事实证明或正式发布批准。

## 本地查看

```bash
python3 -m http.server 8811
```

然后打开 `http://127.0.0.1:8811/`。

## 接入原则

1. 能用规则、schema 或测试解决的问题，不调用模型。
2. 封闭的分类、评分、匹配和筛选问题交给 FastGate。
3. 开放式推理、研究、写代码、调试和执行交给 Codex。
4. 低置信度、结果冲突或高风险动作回退到 Codex、Reviewer 或人工批准。

## 关联项目

- [Jev MCP](https://github.com/blakestone-x/jev-mcp)
- [TypeSafe API 文档](https://api.typesafe.ai/docs)
- [Codex MCP 文档](https://developers.openai.com/docs/extend/mcp)

## License

MIT
