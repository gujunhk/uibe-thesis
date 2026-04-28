# Tasks

- [x] Task 1: 修正页边距和行间距
  - 修改 `\geometry{}` 参数为上/下 3.6cm、左/右 3.1cm
  - 将 `\linespread{1.5}` 替换为 `\setstretch{1.0}` 配合 `\zihao{-4}` 实现固定 22pt 行距（或使用 `fix-cm` + `leading` 方式设定精确值）
  - 确认 `\parindent{2em}` 首行缩进正确，添加 `\raggedbottom` 和段落两端对齐 `\justifying` 设置

- [x] Task 2: 修正英文摘要字体
  - 英文摘要中的英文内容使用 Arial（`\setmainfont{Arial}` 局部设置或用 `\textsf{}` 包裹），中文保持宋体

- [x] Task 3: 添加图片支持
  - 在导言区添加 `\usepackage{graphicx}` 并定义图片搜索路径 `\graphicspath{{figs/}}`
  - 在正文中插入示例图片 `非线性构形状态转移过程示意图.jpg` 作为调试用 demo

- [x] Task 4: 添加表格支持
  - 在导言区添加 `\usepackage{array, booktabs}` 实现三线表
  - 在正文中插入一个 demo 三线表作为示例

- [x] Task 5: 编译验证
  - 使用 `lualatex` + `biber` 编译 `main.tex`，确保无错误且 PDF 生成正确
  - 检查页边距、行距、图片、表格是否正确显示

# Task Dependencies
- Task 1 无依赖
- Task 2 无依赖
- Task 3 无依赖
- Task 4 无依赖
- Task 5 依赖于 Task 1~4 全部完成
