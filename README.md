# 学术论文翻译助手

将英文科研论文完整翻译成中文，并输出适合科研阅读和继续编辑的 Word 文档。当前内容版本：**0.1.2**。

## 两种版本

| 版本 | 源码 | 下载包 | 用途 |
| --- | --- | --- | --- |
| 完整插件版 | [plugin/](plugin/) | [translation-plugin-0.1.2.zip](packages/translation-plugin-0.1.2.zip) | 保存当前 ChatGPT 插件的完整配置、指令、参考规范和 Word 模板 |
| 独立 Skill 版 | [skills/academic-paper-translator/](skills/academic-paper-translator/) | [academic-paper-translator-skill-0.1.2.zip](packages/academic-paper-translator-skill-0.1.2.zip) | 在支持 SKILL.md 的 AI 工具中使用，不依赖原插件的 App 绑定 |

完整插件版保留原插件的包标识和 App 依赖。导入其他账户或环境时，原 App 绑定可能需要重新配置。独立 Skill 版使用名称 `academic-paper-translator`，包含相同的翻译正文规范、排版规范、参考文件与模板。

## 使用方法

### 完整插件版

下载完整插件 ZIP，在支持插件导入的环境中使用。当前插件入口：[学术论文翻译助手](https://chatgpt.com/plugins/plugin_24be45f6f35881918c6ade7bcf1e2b77)。

该链接对应现有插件，是否可访问由其原有权限决定；本仓库公开并不会改变插件的访问权限。

### 独立 Skill 版

1. 下载 Skill ZIP 并解压，保留完整的 `academic-paper-translator/` 文件夹。
2. 按所用 AI 工具的 Skill 安装方式，将整个文件夹放入其技能目录或通过导入功能安装。
3. 提供需要翻译的英文论文及相关补充材料，然后调用该技能，例如：

> 使用 $academic-paper-translator 把这篇英文论文完整翻译成中文并输出 Word。

也可以直接从本仓库复制 `skills/academic-paper-translator/` 文件夹。不能只复制 SKILL.md，否则会缺少配套模板和详细参考规范。

这是工作指令与资源包。使用环境需具备读取 PDF、创建 DOCX、生成 OMML 公式和将 Word 渲染为页面图像的能力；本包不自带模型、Word 软件、字体或渲染程序。

## 翻译与排版要求

- 全文逐段翻译，保持章节、段落、图表、公式、引文及参考文献对应关系。
- 公式使用可编辑的 Word 原生 OMML，表格尽可能重建为可编辑表格。
- 高清原文配图就近置入，配完整中文图注；参考文献保留原文书目信息。
- A4 纵向单栏，页边距上/下/左/右为 2.05/1.85/2.45/2.35 cm。
- 中文宋体，英文和数字 Times New Roman；正文 10.5 pt、约 1.36 倍行距。
- 蓝灰色标题和次要信息，配期刊、DOI 与自动页码。
- 交付前核对完整性，将 Word 渲染为页面图像并逐页检查；修正后重新渲染。
- 译文完整性与科学准确性优先；用户当次明确要求优先于默认排版规范。

模板：[学术论文中文翻译_排版参考模板.docx](skills/academic-paper-translator/assets/学术论文中文翻译_排版参考模板.docx)。

## 验证范围

已检查 Skill 元数据、资源引用、两个 ZIP 的完整性，以及独立 Skill 与原插件正文规范的一致性。此版本尚未在独立 Skill 安装环境中完成整篇论文翻译测试。

## 维护

完整插件源码位于 `plugin/`，独立 Skill 源码位于 `skills/`，可下载包位于 `packages/`。修改翻译要求或模板后，需同步两套源码并重新打包。
