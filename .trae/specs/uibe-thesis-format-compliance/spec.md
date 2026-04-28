# UIBE 学位论文模板格式合规 Spec

## Why
当前 `main.tex` 的页面设置（页边距、行间距等）与《对外经济贸易大学研究生学位论文写作规范（2020修订）》不完全一致，且缺少图片和表格的示例支持，需要对照格式约束文档进行修正和增强。

## What Changes
- 修正页边距：上/下 3.6cm，左/右 3.1cm
- 修正行间距：固定行距 22pt（替代当前的 `\linespread{1.5}`）
- 修正页脚页码格式：Times New Roman 小五号居中
- 修正段落格式：首行缩进 2 汉字符，两端对齐
- 修正英文摘要字体要求：英文使用 Arial 字体
- 添加插图支持：定义 `figs/` 为图片文件夹，插入 `非线性构形状态转移过程示意图.jpg` 作为调试示例
- 添加表格支持：按照格式约束文档实现三线表样式
- 修正中英文摘要与目录的页脚格式与页码连续性

## Impact
- Affected specs: 无（首次创建）
- Affected code: `main.tex`

## ADDED Requirements

### Requirement: 页边距合规
系统 SHALL 将页面边距设置为：上 3.6cm、下 3.6cm、左 3.1cm、右 3.1cm，与《对外经济贸易大学研究生学位论文写作规范（2020修订）》一致。

#### Scenario: 编译后验证页边距
- **WHEN** 用户编译 `main.tex`
- **THEN** 生成的 PDF 页面边距符合上/下 3.6cm、左/右 3.1cm

### Requirement: 行间距合规
系统 SHALL 使用固定行距 22pt 替代当前的多倍行距 `\linespread{1.5}`。

#### Scenario: 正文行距验证
- **WHEN** 用户编译 `main.tex`
- **THEN** 正文段落行距为固定 22pt

### Requirement: 图片支持
系统 SHALL 支持在正文中插入图片，使用 `figs/` 文件夹存放图片文件，并提供一张调试用示例图片 `非线性构形状态转移过程示意图.jpg`。

#### Scenario: 插入调试图片
- **WHEN** 用户在正文中引用 `figs/非线性构形状态转移过程示意图.jpg`
- **THEN** 编译后 PDF 中正确显示该图片

### Requirement: 表格支持
系统 SHALL 支持在正文中插入三线表，符合格式约束文档的表格排版要求。

#### Scenario: 插入三线表示例
- **WHEN** 用户在正文中插入 demo 表格
- **THEN** 编译后 PDF 中正确显示三线表样式

### Requirement: 英文摘要字体合规
系统 SHALL 将英文摘要中英文内容设置为 Arial 字体，中文内容设置为宋体。

#### Scenario: 英文摘要字体验证
- **WHEN** 编译 `main.tex`
- **THEN** 英文摘要中英文部分使用 Arial 字体，中文部分使用宋体

## REMOVED Requirements
无。
