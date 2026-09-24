# 秋夕韩语店铺导入包

## 后台上传

在 Ops → 配送目录 → 批量导入中选择 `chuseok-ko-catalog.json`，执行“预检并准备图片”，核对实际新增/更新摘要与字段问题，再确认整批导入。**不要把 ZIP 当作导入文件上传**；ZIP 仅供交付和备份。

已做文件自检，待 Ops 预检。本包没有执行后台导入，也没有复制或改写任何配送方式。

## 内容

- `chuseok-ko-catalog.json`：可供 Ops 预检的 UTF-8 JSON，韩语 `ko`，1 个分类、1 家店铺、10 个商品，价格 18–198 ICE。
- `images/`：11 张已公开托管的 WebP 图片本地备份，包含店铺封面和 10 张菜品图。
- `image-manifest.json`：本地文件、GitHub 路径与公开 URL 的一对一映射。
- `qa-contact-sheet.jpg`：整套图片总览。

分类、店铺和商品沿用原秋夕店铺的 `external_id`，再次导入会按这些编号更新，而不是按名称新建。仅图片 URL 切换到 `images/chuseok/ko/commercial-v2/`，其他字段及价格不变。分类与店铺共用封面 URL，但按不同用途准备图片，因此需要 12 项 `(用途, URL)` 图片准备记录；没有独立店铺图标。

公开素材目录：https://github.com/tristainsummer/delivery-catalog-assets/tree/main/images/chuseok/ko/commercial-v2
