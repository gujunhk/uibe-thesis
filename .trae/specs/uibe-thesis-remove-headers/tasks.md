# Tasks

- [x] Task 1: 修正页眉页脚设置
  - 取消 `\fancyhf{}` 的注释以清空所有默认页眉页脚
  - 添加 `\fancyfoot[C]{\zihao{-5}\rmfamily\thepage}` 设置页脚居中 Times New Roman 小五号页码
  - 保留 `\renewcommand{\headrulewidth}{0pt}` 无页眉线

- [x] Task 2: 编译验证
  - 使用 `lualatex` + `biber` 编译 `main.tex`，确保无错误
  - 检查 PDF 正文页无页眉、页脚页码居中且格式正确

# Task Dependencies
- Task 2 依赖于 Task 1
