# 2026年度营销中心·即时激励表彰公示

## 界面说明

- 荣誉卡片白底约 **31% 透明度**（较原先降低一半），背景更易透出
- 左上：**安恒信息** Logo（100% 不透明 + 阴影）
- 背景居中：**营销中心即时激励** 水印（与标题同字体，低透明度）
- 各部门 Tab 内容最下方：**查看即时激励制度**（弹窗约页面 70%）
- 页脚：营销综合管理部 · 版权所有

## 制度与附件

- 综合管理部的制度全文在 `js/policies.js` → `management`
- 行销部制度在 `js/policies.js` → `sales`
- 报名表：`assets/营销综合管理部即时激励提名表.docx`、`assets/行销部即时激励提名表.docx`

## 上传照片与打包

- **批量导入**：将照片放入任意文件夹后运行  
  `powershell -ExecutionPolicy Bypass -File .\scripts\import-photos.ps1 -PhotoDir "你的照片文件夹路径"`  
  会生成 `js/photos-data.js`（Base64 内嵌，按文件名匹配姓名；`周伟琴` 会自动对应 `周伟芹`）。
- **单张上传**：也可点击圆形头像本地上传（仅当前浏览器会话）。
- 完成后点「打包下载公示页」。**支持双击 `index.html`（file://）打包**，无需本地服务器；照片已写入配置，他人打开单文件 HTML 即可看到头像。

修改 `css/style.css` 后请运行：`.\scripts\sync-export-css.ps1`

分发：请使用页面内 **「打包下载公示页」**（Logo 与样式已 Base64 内嵌）。勿用浏览器「另存为」，否则会丢失 Logo。

若更换 `assets/logo-anheng.png`，需重新生成 `js/logo-data.js`（与 `export-css.js` 同样方式同步）。

## 编辑表彰文字

修改 `js/config.js` 后刷新页面即可。

### 事迹正文加粗

在 `text`、`keyItems`、`achievements` 中用成对的 `**` 包裹需要加粗的文字，例如：

```javascript
text: '项目已中标，金额**280万元**。'
```

显示为：项目已中标，金额**280万元**。姓名、部门、关键词标签请保持纯文本，不要使用 `**`。
