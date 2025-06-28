# Karnaugh Map LaTeX Generator

这是一个用于交互式生成 LaTeX 格式卡诺图代码的 Web 工具，支持 2 至 4 个变量的卡诺图绘制，并提供可视化的圈选功能，帮助你快速生成 `\begin{karnaugh-map} ... \end{karnaugh-map}` 格式的代码。

This is a web tool for interactively generating LaTeX code for Karnaugh maps. It supports 2 to 4 variables and provides visual circle selection, making it easy to create code in the format `\begin{karnaugh-map} ... \end{karnaugh-map}`.

## 🎯 功能特点 | Features

* ✅ 支持 2\~4 个变量的卡诺图生成
  ✅ Supports Karnaugh maps with 2 to 4 variables
* ✅ 输入 minterms 与 don't care 项
  ✅ Enter minterms and don't care terms
* ✅ 自定义 don't care 显示符号（默认 X）
  ✅ Customizable don't care symbol (default: X)
* ✅ 自动填补剩余项为 0（可选）
  ✅ Optionally auto-fill remaining cells with 0
* ✅ 可视化点击格子进行 implicant 圈选
  ✅ Clickable grid for visual implicant selection
* ✅ 自动生成标准 LaTeX 代码，兼容新版 `karnaugh-map` 宏包
  ✅ Auto-generates LaTeX code compatible with the latest `karnaugh-map` package

## 🖱 使用方法 | Usage

1. 打开 HTML 文件（双击或拖入浏览器）
   Open the HTML file in a browser
2. 设置变量数量（2\~4）与变量名
   Set the number of variables and their names
3. 输入 minterms 和 don't care 项
   Enter minterms and don't care terms
4. 勾选“Auto-fill remaining cells with 0”自动补全 0 项（可选）
   Check "Auto-fill" to automatically fill the rest with 0 (optional)
5. 点击格子选择要圈选的 minterm
   Click on grid cells to select minterms for grouping
6. 点击 “Add Implicant” 自动添加 `\implicant{起}{终}[...]`
   Click "Add Implicant" to generate an `\implicant` line
7. 点击 “Generate LaTeX” 生成完整 LaTeX 代码
   Click "Generate LaTeX" to get the full code
8. 将生成的代码复制粘贴至你的 LaTeX 文档中使用
   Copy and paste the result into your LaTeX document

## 📦 LaTeX 使用示例 | Example LaTeX Code

```latex
\documentclass{article}
\usepackage{karnaugh-map}
\begin{document}

\begin{karnaugh-map}[4][4][1][$C$][$D$][$A$][$B$]
  \minterms{0, 2, 5, 7, 8, 10, 13}
  \terms{1}{$X$}
  \terms[0]{3, 4, 6, 9, 11, 12, 14, 15}
  \implicant{0}{2}[0,2]
\end{karnaugh-map}

\end{document}
```

## 📚 依赖环境 | Requirements

* 使用时仅需浏览器支持，无需网络连接
  Only requires a web browser, no internet needed
* 生成的代码需配合 LaTeX `karnaugh-map` 宏包使用
  Generated code requires the LaTeX `karnaugh-map` package

---

由 ChatGPT 协助开发 💻 | Powered with ❤️ by ChatGPT
