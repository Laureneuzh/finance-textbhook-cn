# 金融学基础：七章中文译稿

本目录提供七章完整简体中文译稿、中文 LaTeX 编译主文件和合并 PDF。原文的章节层级、案例、图表、公式、脚注、章末总结、讨论题、应用题、数据练习、AI 实验和参考文献均予保留。参考文献保留原文题名及出版信息，并附中文题名；关键术语提供中英文对照。

## 阅读与编辑

- 现有 `finance-textbook-zh.pdf` 为前五章的合并 PDF；加入第七章后，请用 `main_zh.tex` 重新编译生成七章版本。
- 编辑或编译入口：`main_zh.tex`。
- 五个章节文件沿用英文文件名，正文为中文；英文原稿位于仓库根目录。
- 章节顺序：金融的本质；货币、支付与流动性架构；信息经济学与金融契约；金融中介与金融结构；金融估值的逻辑；利率与资本配置；货币市场与短期流动性契约。

## 编译

安装包含中文支持的 TeX Live 或 MiKTeX，在本目录运行：

```shell
latexmk -xelatex -interaction=nonstopmode -halt-on-error main_zh.tex
```

也可连续运行三次：

```shell
xelatex -interaction=nonstopmode -halt-on-error main_zh.tex
```

主文件使用 `ctexbook` 和 TeX 发行版自带的 Fandol 字体，不依赖特定操作系统的中文字体。所需宏包包括 `amsmath`、`amssymb`、`booktabs`、`tabularx`、`enumitem`、`tikz`、`tcolorbox`、`fancyhdr` 和 `hyperref`。TikZ 图示保留为可编辑矢量图。

本目录随附的 PDF 使用描述性文件名；自行编译时默认生成 `main_zh.pdf`，二者是同一主文件的输出。

## 校对说明

- 正文采用中国大陆金融学常用译法，保留原文案例背景、货币单位及数值；中文叙述中的金额按元、万元或亿元等对应换算。
- 七章的章节层级、习题条目、图表与交叉引用标识经过结构对照；前五章的 65 个展示数学块的符号与运算结构和英文原稿一致，仅翻译说明文字。
- 全部交叉引用均在本七章内定义；前五章合并 PDF 已经过多轮 XeLaTeX 编译及逐页版面检查。第七章已核对公式及交叉引用；本次环境缺少 `ctexbook.cls`，未完成七章合并编译。
- 教材中的 AI 实验、数据练习和案例分析要求均为翻译内容，未代为执行或作答。
- 本稿依据原文翻译，不增补新的事实主张或改变原文论证。原稿中的重复段落按原文保留。

源版本：前五章为仓库根目录于 2026 年 11 月 1 日上传的英文 `.tex` 文件；第七章依据 2026 年 11 月 2 日提供的 `Interest_Rates_and_Capital_Allocation.tex` 翻译。

## 第七章外部图文件

第七章引用 `ChinaBond_10Y_Yields_2016_2026.pdf` 和 `China_Government_Yield_Curves_Typical.pdf`。本次未提供这两张原图，现有仓库中亦未找到。译稿保留图号、图题、来源、引用与原文件名；缺图时显示说明框。将原图放入本目录即可自动显示。主文件已增加 `pgfplots` 支持。

## 第七章（2026 年 11 月 8 日）

已加入 `Money_Markets_and_Short_Term_Liquidity_Contracts.tex` 中文译稿，并接入主文件。使用随附英文正文翻译，保留公式、交叉引用和原有重复段落。新增 `makecell` 宏包支持原稿表头。现金流例子开头为 45 天回款，下文与图示为第 28 天，已保留并加译注，待作者核定。当前 PDF 仍为前五章版本。

本次另附的第八至第十五章为 `.aux` 文件，仅含目录、标签及编译信息，没有正文。英文仓库的同名 `.tex` 也仅为提纲，部分标题与附件不一致。因此未将提纲冒充完整译稿，以下章节待补充正文 `.tex` 后翻译：

- `Bond_Markets_and_Debt_Contracts.tex`
- `Stock_Markets_and_Equity_Claims.tex`
- `Foreign_Exchange_Markets_and_Cross_Border_Finance.tex`
- `Derivatives_Markets_and_Contingent_Claims.tex`
- `Commercial_Banks_Credit_Intermediation_and_Liquidity_Creation.tex`
- `Investment_Banks_Capital_Raising_and_Capital_Market_Intermediation.tex`
- `Asset_Management_and_Institutional_Investment.tex`
- `Insurance_and_Risk_Sharing_Institutions.tex`
