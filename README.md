# 宝石物性检索 3.1 / Gem Property Finder 3.1

此文件夹是 3.1 的静态发布副本，包含当前已保存的 103 项手动校对数据。无需安装依赖或构建。
This is a standalone static copy of version 3.1, including 103 saved, manually reviewed records. No dependencies or build step are required.

## 上传 / Upload

将本文件夹里的文件上传到 GitHub 仓库根目录（让 index.html 位于根目录）。然后在仓库 Settings → Pages 中选择从分支部署，选择对应分支及根目录。
Upload the contents of this folder to the repository root, with index.html at the root. In Settings → Pages, deploy from the selected branch and root folder.

## 包含功能 / Features

- Chart A / 全部 / Chart B；RI、SG、颜色、光性、透明度及 LW/SW 筛选。
- 选择 ADR 按 SR 搜索；拼合石始终放在最后。
- 默认按 RI、SG 与标称值的综合相对偏差排序；区间取中点，独立读数取最近值。
- 展开按钮右侧分别显示 RI、SG 匹配百分比。这不是鉴定正确率；Range 和测量误差仍用于筛选。
- Chart selection and RI, SG, colour, optical character, transparency and LW/SW filters.
- ADR searches SR; assembled stone remains last.
- Default equal-weight relative-distance ranking against nominal RI/SG values, using interval midpoints or the nearest separate reading.
- Separate RI/SG matching percentages, not identification probabilities; source ranges and measurement tolerances still control inclusion.

## 2026-10-19 修复 / Repairs

- 荧光以手动勾选为准：已勾选为有，未勾选为无；不再用旧原文补成“未知”或“有”。 / Saved LW/SW selections are authoritative: checked = yes, unchecked = no; legacy prose does not override them.
- RI/SG 仅接受正有限小数（支持小数逗号）；无效输入会提示并跳过该条件，其他有效条件继续生效。 / RI/SG require finite positive decimals; invalid inputs are visibly flagged and skipped without disabling other valid filters.
- 手机横向滚动后展开详情，会将详情移入视野；已保存的空颜色备注不再被旧染色备注覆盖。 / Expanded mobile details enter view; saved blank colour notes stay blank.
- GIA 官方中文名未查证的 Chlorastrolite、Saussurite、Prosopite 仍保留“中文名待核”。 / Those three names remain pending official GIA Chinese verification.

## 数据与发布说明 / Data and publishing notes

review-overrides.js 包含已应用的手动校对数据，必须一起上传。本文件夹是独立快照，今后本地校对修改不会自动更新到 GitHub。
review-overrides.js contains applied manual corrections and must be uploaded. This is a snapshot; future local edits will not automatically update GitHub.

未包含校对台、数据库、草稿、修改日志、备份、原图或测试。请勿另外上传这些私人工作文件。
The editor, database, drafts, logs, backups, source photos and tests are excluded. Do not add those private working files.

原始资料来自 GIA Gem Property Chart A、B（© 1992 The Gemological Institute of America）。公开发布前请确认转载和使用权限。本工具用于课堂参考，不是 GIA 官方软件，也不能替代完整鉴定。
Source material: GIA Gem Property Charts A and B, © 1992 The Gemological Institute of America. Confirm redistribution rights before public publication. This classroom reference is not official GIA software and does not replace full gemological identification.

## 2026-10-27 界面与本地导入 / UI refresh and local import

- 新布局：左侧筛选栏（可折叠分组、条件计数、一键重置），右侧结果；已选条件以标签显示，可单独移除；手机端结果改为卡片，并有“查看结果”快捷条；支持深色模式。 / New sidebar + results layout, removable filter chips, mobile cards, dark mode.
- 我的宝石（手动录入）：点击右上角“添加我的宝石”，填写名称、RI、SG、光性、颜色、透明度、荧光后保存；可一键“用当前筛选值填入”，可随时编辑或删除。记录与 Chart A/B 一起筛选、排序，带紫色“我的”标签，可在“数据范围 → 我的”中单独查看。需要时也可在弹窗底部“批量导入文件”中导入 CSV / JSON。 / Add your own gems by hand (or bulk-import CSV/JSON); they are searched alongside Chart A/B.
- 导入数据仅在浏览器内解析，保存在当前标签页（sessionStorage），关闭标签页即清除，不会上传。缺失字段不作为排除条件。 / Parsed locally, kept only for the current tab, never uploaded.

## 2026-10-27 鉴定分类 / Identification

- 每个宝石详情卡顶部新增“鉴定分类 / Identification”：族 Group、系列 Series、种 Species、变种 Variety、商业名 TN（中英对照）；合成品、有机宝石、岩石等附简短说明。 / Each gem card now lists Group, Series, Species, Variety and Trade name.
- 数据在 identification-data.js（必须一起上传）。依据 GIA Gem Encyclopedia、mindat.org、IGS 等常用宝石学资料整理，并对少见条目做了网上核对；标注“误称 / misnomer”的商业名具误导性，不能作为鉴定名称。课堂使用前建议按教材再核一遍。 / Data lives in identification-data.js (upload it too); compiled from standard gemmological references.
- 名称搜索也会匹配变种和商业名，例如搜 tanzanite、帕拉伊巴、Larimar。手动录入的宝石可在“更多信息”中填写这 5 项。 / Search also matches varieties and trade names; manual entries can include these fields.
