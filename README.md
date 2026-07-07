# Privacy · 应用隐私政策

> HuangYiwei 开发的 iOS 应用的隐私政策（Privacy Policy）页面仓库。

本仓库托管各款应用的隐私政策 HTML 页面，**一款应用一个子目录**，每个目录下一个自包含的 `index.html`（内联 CSS、零外部依赖）。页面通过 GitHub Pages 公开访问，供 App Store 审核与用户随时查阅。

四款应用有一个共同的隐私主张：**100% 离线、纯本地运行**——不收集任何个人信息、不联网传输、无账号系统、无第三方分析 / 广告 / 云同步。

---

## 收录的应用

| 应用 | 子目录 | 最后更新 | 简介 | 在线访问 |
| --- | --- | --- | --- | --- |
| **BrainPower 大脑体能馆** | [`brain_power/`](brain_power/index.html) | 2026-03-12 | 基于循证心理学（CBT · ACT · MBCT · CBTi）的心理健康训练应用，含 PHQ9 / GAD7 / ISI 评估、正念训练、心情与睡眠日记、番茄钟等 | `https://huanghyw.github.io/privacy/brain_power/` |
| **记忆督学官** | [`mem_card/`](mem_card/index.html) | 2026-01-30 | 基于艾宾浩斯遗忘曲线的智能记忆卡片应用 | `https://huanghyw.github.io/privacy/mem_card/` |
| **存钱管家 · Money Saving Manager** | [`money_saving_manager/`](money_saving_manager/index.html) | 2026-06-24 | 通过结构化储蓄计划（365 天递增 / 52 周挑战 / 12 个月 / 每日固定 / 自由存）＋打卡连击养成本地存钱习惯 | `https://huanghyw.github.io/privacy/money_saving_manager/` |
| **黑白空间 · B&W Space** | [`film_darkroom/`](film_darkroom/index.html) | 2026-07-07 | 离线黑白胶片冲洗工具，内置显影数据库、显影倒计时（多阶段 / 搅拌提醒 / 温度补偿），支持自录配方与 JSON 导入导出 | `https://huanghyw.github.io/privacy/film_darkroom/` |

> 在线访问地址需在本仓库 **Settings → Pages** 中启用「从 `main` 分支 `/root` 托管」后生效。

---

## 共性隐私主张

每份政策的内核一致，差异只在「本地存储了哪些数据」「用了哪些权限」：

- **不收集**：姓名 / 邮箱 / 电话、位置、设备广告标识符（IDFA 等）、通讯录、生物识别、网络浏览历史等一切可识别个人信息。
- **不传输**：所有数据仅存设备本地，无任何远程服务器、无云端同步。
- **不共享 / 不出卖**：不与广告商、分析商、社交平台、金融机构或任何第三方共享。
- **不使用**：用户行为分析（GA / Firebase）、广告、社交登录、云存储、远程推送、崩溃上报等第三方服务。
- **本地存储**：仅记录与应用功能相关的必要数据（如训练记录、卡片内容、储蓄金额），靠 iOS 沙盒隔离保护；导出备份采用密码 AES 加密。
- **用户控制权**：可在应用内随时查看、删除、导出全部数据；卸载即彻底清除。

---

## 目录结构

```text
privacy/
├── README.md
├── brain_power/
│   └── index.html            # BrainPower 大脑体能馆 隐私政策
├── mem_card/
│   └── index.html            # 记忆督学官 隐私政策
├── money_saving_manager/
│   └── index.html            # 存钱管家 · Money Saving Manager 隐私政策
└── film_darkroom/
    └── index.html            # 黑白空间 · B&W Space 隐私政策
```

每个 `index.html` 都是独立的静态页面：统一的中英文字体栈、卡片式排版、移动端响应式（`@media (max-width: 600px)`），底部附「联系我们」与「适用法律（中华人民共和国法律法规）」区块。

---

## 新增一款应用的隐私政策

约定：新建一个与应用（或 Bundle）同名的子目录，放入一个自包含的 `index.html`。建议从现有页面复制模板，再按新应用调整：

1. **本地存储的数据**（§2.2）——该应用实际写入了哪些本地数据。
2. **权限使用说明**（§三）——该应用实际请求了哪些系统权限及其用途与拒绝影响。
3. **第三方组件**（§5.1）——该应用 `pubspec.yaml` 实际依赖的库。
4. 顶部「最后更新日期」与底部「联系我们」中的对应字段（应用名、Bundle ID、更新日期）。

> 模板要求与现有页面一致：纯静态、无外链依赖、可被 GitHub Pages 直接托管；草稿文件请遵循 [`.gitignore`](.gitignore) 的排除规则（`draft*.html` / `*_draft.*` 等不会入库）。

---

## 开发者

- **应用名**：见上表
- **开发者**：HuangYiwei
- **联系邮箱**：<huanghyw@gmail.com>
- **仓库**：[github.com/huanghyw/privacy](https://github.com/huanghyw/privacy)
