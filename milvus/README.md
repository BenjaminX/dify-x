RAG 的演进之路：从“状态”到“记忆” — Dify × Milvus

## 简述

- 一套基于 Reveal.js 的演讲幻灯片，面向开发者与数据平台团队，主题覆盖 Naive / Advanced / Agentic RAG、Knowledge Pipeline、外环评估与 Dify × Milvus 的协同实践。
- 视觉遵循 Dify 品牌：Dify Blue `#0033FF`、极简几何与弥散渐变、轻手绘纹理点缀。

## 使用方式

1. 在线访问
   - 作为 dify-x 站点的一部分：https://crazywoola.github.io/dify-x/milvus/index.html

2. 本地预览
   从仓库根目录启动任意 HTTP 服务器：
   ```bash
   python3 -m http.server 8000
   # 访问 http://localhost:8000/milvus/index.html
   ```

## 快捷键

- 主题切换：在幻灯片页面按键 `1`（Swiss）/ `2`（Atelier）/ `3`（Ukiyo）
- 演讲者备注：按 `s` 打开 Presenter Notes

## 项目结构

- `index.html`：中文主页面（`index_en.html` 为英文版）
- `styles/`：主题与样式文件
  - `base.css`：基础样式
  - `dify-theme.css`：品牌主题变量
  - `theme-swiss.css` / `theme-atelier.css` / `theme-ukiyo.css`：三套主题变体
- `assets/`：图片资源（Logo 等）
- `context.md` / `target_audience.md`：内容与受众设定
- `AGENTS.md`：本目录的工程约定

## 品牌与排版

- 英文：Söhne / Söhne Mono（本地安装则自动使用）
- 中文：Mi Sans（回退：PingFang SC / Noto Sans SC / 等）
- 默认字号较大（h1 ≈ 118px，h2 ≈ 60–66px，正文 ≈ 34–36px），强调可读性与舞台呈现。

## 自定义与扩展

- 调整强调色：`styles/dify-theme.css` 中的 `--dify-primary`
- 添加 / 移除弥散渐变：给 `<section>` 增加 / 移除 `class="accent"`
- 添加新主题：在 `styles/` 新增 CSS，并在 `index.html` 的快捷键切换中注册

## 许可

- 幻灯片结构与代码开源；Logo 与品牌元素归 Dify 所有，请在品牌规范内使用。
