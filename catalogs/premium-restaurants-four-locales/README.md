# 四地区豪华餐厅 Ops 上传包

本文件提交 4 家餐厅，每家仅含 666 ICE 与 888 ICE 两个套餐，共 8 个商品，语言为 ja、ko、en、zh-Hant。此包不修改既有分类或配送方式；实际新增/更新数量以 Ops 预检为准。

## 文件

- premium-restaurants-four-locales-catalog.json：Ops 批量导入 JSON。
- image-manifest.json：12 张主图/套餐图与 4 个店铺 icon 的 GitHub 路径、用途、大小与 SHA-256。
- validation-report.json：本地契约自检结果。
- images/：已发布到 GitHub 的 12 张 WebP 原文件，目录结构与 image_url 一致。
- icons/：用户提供的统一 PNG icon，按四个店铺 external_id 分别存放，目录结构与 icon_url 一致。

## GitHub 发布状态

- 仓库：https://github.com/tristainsummer/delivery-catalog-assets
- 素材提交：1c70a9adcb5b66d213f7e8615d90fd34ef31de24
- 当前状态：已推送到公开仓库的 main 分支，16 个公开图片链接均通过下载和 SHA-256 校验。

JSON 的图片链接固定到素材提交，不随 main 分支后续更新改变。image-manifest.json 中保留了 16 个链接的公开下载验证结果。GitHub 仅托管素材；Ops 仍需预检、转存图片及确认导入。

## Ops 流程

1. 只选择 premium-restaurants-four-locales-catalog.json。
2. 执行“预检并准备图片”。
3. 核对目标环境实际新增/更新摘要；本文件提交 4 家店铺、8 个商品，分类与配送方式均为 0 条。不能仅凭本文件判断新增数。
4. 图片准备完成后再次预检，再确认导入。

依赖目标环境已存在以下分类 external_id：category-ja-sushi、category-ko-korean-bbq、category-en-bbq、category-zh-Hant-bento-rice。

保留原 external_id、名称、描述、商品类型、规格及 666/888 ICE 价格；本包商品类型仍为 default，不是 DIY 商品。原待发布压缩包未覆盖。

已做文件自检，待 Ops 预检。待转存图片与图标共 16 个 URL。
