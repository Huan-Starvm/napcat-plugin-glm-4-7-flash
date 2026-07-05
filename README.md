# GLM-4.7-Flash NapCat 插件

这是一个 NapCatQQ 插件，用于对接智谱 GLM-4.7-Flash 聊天模型。

## 功能

- 调用 `glm-4.7-flash` 进行聊天。
- 群聊默认只在 `@目标 QQ` 或回复 `目标 QQ` 发出的消息时触发。
- `目标 QQ` 留空时，插件会自动读取当前登录 QQ。
- 支持每个群成员或私聊独立的短期会话记忆。
- 支持 429 / 5xx 临时错误自动重试。
- 支持 NapCat 插件配置面板。

## 安装

```text
plugins/
└─ napcat-plugin-glm-4-7-flash/
   ├─ package.json
   ├─ index.mjs
   ├─ icon.png
   └─ README.md
```

启用插件后，在配置里填写 `GLM API Key`。

## 常用配置

- `GLM API Key`: 智谱 BigModel API Key，也可使用环境变量 `ZHIPUAI_API_KEY` 或 `GLM_API_KEY`。
- `触发 QQ`: 群聊中被 @ 或被回复的 QQ。留空时自动使用当前登录 QQ。
- `群聊触发方式`: 可选 `@ 或回复`、`仅 @`、`仅回复`。
- `允许私聊直接触发`: 默认关闭。
- `请求超时毫秒`: 默认 `120000`。
- `失败重试次数`: 默认 `2`。
- `重试基础间隔毫秒`: 默认 `2500`。

## 图标

- `icon.png`: 插件市场图标，512x512。
- `icon.svg`: 可编辑源文件。
