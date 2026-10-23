# Lumen Select · Nebula UI

星云主题的选品情报云界面：登录页 + 选品报告详情页。纯静态 HTML / CSS / JS，无构建步骤、无外部依赖。

| 页面 | 文件 | 说明 |
| --- | --- | --- |
| 登录页 | [`nebula-login.html`](nebula-login.html) | 单文件。右侧 WebGL2 体积星云 + Canvas 2D 星轨 / 星尘 + 静态预渲染星核；左侧登录表单与校验、跳过 / 重播、响应式、`prefers-reduced-motion`、WebGL2 降级 |
| 报告详情页 | [`report.html`](report.html) | Nebula 主题：摘要指标、结论筛选、排序表、7 张决策卡（默认折叠）、`[E#]` 证据定位、降低光效、导出 XLS（演示） |
| 主题样式 | [`assets/tokens.css`](assets/tokens.css) · [`assets/nebula-theme.css`](assets/nebula-theme.css) | 设计 token、基础组件、星空背景 / 玻璃卡片 / 发光状态 |

`index.html` 只负责跳转到登录页。

## 本地预览

```bash
python3 -m http.server 4173
# 打开 http://localhost:4173/
```

## 演示说明

- 登录为纯前端演示：任意合法邮箱 + 6 位以上密码即可，不发任何请求、不保存密码。登录成功后进入报告详情页。
- 报告页数据均为示例数据。
- 登录页快捷键：`Esc` 跳过开场，`R` 重播（输入框内不触发）。
- 调试参数：登录页 `?nogl` 强制走 WebGL2 降级；报告页 `?state=error` / `?state=empty` / `?state=exportfail` 查看错误 / 空 / 导出失败状态。

## 部署

GitHub Pages，从 `main` 分支根目录发布。
