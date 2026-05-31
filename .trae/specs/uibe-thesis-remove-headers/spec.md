# 移除页眉 Spec

## Why
格式约束文档明确规定"无需加页眉"。当前 [main.tex:L91](file:///e:/Projects/Github/gujunhk/uibe-thesis/main.tex#L91) 中 `\fancyhf{}` 被注释掉，导致 fancyhdr 默认页眉（章节标题）会出现在正文页面中，不符合规范。

## What Changes
- 取消注释 `\fancyhf{}` 以清空所有页眉页脚默认值
- 显式设置页脚居中页码：Times New Roman 小五号（与格式文档一致）
- 保留 `\headrulewidth{0pt}` 无页眉线

## Impact
- Affected specs: `uibe-thesis-format-compliance`
- Affected code: [main.tex:L89-L92](file:///e:/Projects/Github/gujunhk/uibe-thesis/main.tex#L89-L92)

## MODIFIED Requirements
### Requirement: 页眉页脚合规
系统 SHALL 确保正文页面无页眉，页脚居中显示 Times New Roman 小五号页码。

#### Scenario: 正文页无页眉
- **WHEN** 编译 `main.tex`
- **THEN** 正文各页顶部无章节标题等页眉内容

#### Scenario: 页脚页码格式
- **WHEN** 编译 `main.tex`
- **THEN** 正文各页页脚居中显示 Times New Roman 小五号阿拉伯数字页码
