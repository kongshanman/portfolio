# AetherCode Labs：纯网页创建与部署教程

适用账号：`kongshanman`。所有创建、编辑、保存和发布操作都在 `github.com` 完成，无需终端、Git 命令或本地开发环境。教程同时列出中英文按钮名；GitHub 自动翻译可能稍有不同。

本教程可用于日后维护或重新搭建。已经创建的仓库直接进入编辑步骤，已经上线的官网不用重复创建。网页填写通常可在约十分钟内完成；登录验证、授权和 GitHub 部署等待另计，不能保证十分钟内全部完成。

## 0. 先分清四个仓库和四份物料

| 用途 | 仓库名 | 要保存的文件 | 内容来源 |
| --- | --- | --- | --- |
| GitHub 个人主页 | `kongshanman` | 根目录 `README.md` | [物料 1：Profile README](materials/profile-README.md) |
| AST 项目 | `ast-refactor-core` | 根目录 `README.md` | [物料 2：AST 项目 README](materials/ast-refactor-core-README.md) |
| 测试生成项目 | `cli-testgen` | 根目录 `README.md` | [物料 3：CLI 项目 README](materials/cli-testgen-README.md) |
| 静态官网 | `portfolio` | 根目录 `index.html` | [物料 4：完整 HTML](index.html) |

三个 README 均为可直接粘贴的英文材料。打开对应文件后，点击 **Raw / 原始内容**，在原始文本页面按 `Ctrl+A`、`Ctrl+C`（Mac 用 `Command+A`、`Command+C`）复制；不要复制 GitHub 页面按钮或渲染后的网页。

官网入口：<https://kongshanman.github.io/portfolio/>。

`kongshanman` 是个人 Profile 仓库；`portfolio` 是项目型 Pages 仓库。若以后使用无路径的个人 Pages 地址，仓库必须叫 `kongshanman.github.io`，不是 `kongshanman`。这次统一使用 `portfolio`，不迁移已发布的网址。

## 1. 创建个人主页仓库

1. 登录 GitHub，确认右上角头像属于 `kongshanman`。
2. 点击网页右上角 **＋**，选择 **New repository / 新建仓库**。也可以直接打开 [预填创建页面](https://github.com/new?owner=kongshanman&name=kongshanman&visibility=public&description=AetherCode%20Labs%20-%20independent%20developer%20tooling%20studio.)。
3. **Owner / 所有者** 选 `kongshanman`。
4. **Repository name / 仓库名称** 填 `kongshanman`。这里必须与账号用户名完全一致，品牌名称写在 README 中。
5. **Description / 描述** 填：`AetherCode Labs - independent developer tooling studio.`
6. **Choose visibility / 选择可见性** 选 **Public / 公开**。
7. 将 **Add README / 添加自述文件** 的开关设为 **On / 开启**。
8. **Add .gitignore** 保持 **None / 无**；**Add license / 添加许可证** 暂时保持 **None / 无**，稍后粘贴本套 MIT 许可证。
9. 点击底部绿色 **Create repository / 创建仓库**。

个人主页展示需要：公开的同名仓库、根目录里非空的 `README.md`。[GitHub 官方 Profile 说明](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme)

### 粘贴并保存 Profile README

1. 在新仓库的 **Code / 代码** 页点击文件列表中的 `README.md`。
2. 点击文件内容区域右上方的 **铅笔图标（Edit this file / 编辑此文件）**；不是右上角个人头像，也不是仓库 Settings。
3. 先点击代码编辑框内部，再按 `Ctrl+A`（Mac 用 `Command+A`）全选原内容。
4. 粘贴物料 1 的完整原始 Markdown。
5. 点击 **Preview / 预览**，检查标题为 `AetherCode Labs`，徽章、Mission 和 Tech Stack 均存在。
6. 点击 **Commit changes… / 提交更改**。
7. 弹窗的提交说明填 `docs: add AetherCode Labs profile`。对本次新建且无分支保护的个人仓库，选择 **Commit directly to the main branch / 直接提交到 main 分支**。
8. 再点击弹窗内绿色 **Commit changes / 提交更改**，等页面返回文件视图。
9. 打开 <https://github.com/kongshanman>，确认 Profile README 出现在个人主页。仓库里有 README 并不意味着任意名称的仓库都会展示在个人主页。

文件编辑与提交入口参考 [GitHub 官方编辑说明](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files)。如果按钮变成 **Propose changes**，先确认登录账号和仓库所有者是否正确；本教程不要求修改任何分支保护规则。

## 2. 创建两个独立项目仓库

分别打开：

- [创建 ast-refactor-core](https://github.com/new?owner=kongshanman&name=ast-refactor-core&visibility=public&description=AetherCode%20Labs%20-%20AST%20analysis%20and%20code%20smell%20detection%20specification.)
- [创建 cli-testgen](https://github.com/new?owner=kongshanman&name=cli-testgen&visibility=public&description=AetherCode%20Labs%20-%20unit-test%20and%20mock%20generation%20CLI%20specification.)

每次都确认 **Owner = kongshanman、Public、Add README = On**，`.gitignore` 和许可证先选 **None**，然后点击 **Create repository**。预填链接只填写表单，不会自动创建仓库；若提示名称已存在，进入已有仓库，不要改名另建。

依照第 1 节的“点击 README → 铅笔 → 编辑框全选替换 → Preview → Commit changes → 弹窗再次 Commit changes”步骤：

| 仓库 | 粘贴内容 | 提交说明 |
| --- | --- | --- |
| `ast-refactor-core` | 物料 2 | `docs: add AST analysis specification` |
| `cli-testgen` | 物料 3 | `docs: add test generation CLI specification` |

保存后应分别能打开：

- <https://github.com/kongshanman/ast-refactor-core>
- <https://github.com/kongshanman/cli-testgen>

新建仓库和预填参数参考 [GitHub 官方创建说明](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)。

### 为三个仓库加入 MIT 许可证

对 `kongshanman`、`ast-refactor-core`、`cli-testgen` 分别执行一次：

1. 复制 [本套 LICENSE 的完整原始文本](LICENSE)。
2. 打开目标仓库的 **Code / 代码** 页。
3. 在文件列表上方点击 **Add file / 添加文件 → Create new file / 创建新文件**。
4. 顶部 **Name your file / 文件名** 填 `LICENSE`，不带扩展名。
5. 在编辑框中粘贴完整文本，保留 `Copyright (c) 2026 AetherCode Labs`。
6. 点击 **Commit changes…**，提交说明填 `docs: add MIT license`，选择直接提交到 `main`，再点击弹窗的 **Commit changes**。

如果 `LICENSE` 已存在，点击该文件的铅笔编辑，不要创建重名文件。README 中的 License 徽章应能打开相应仓库的许可证。

## 3. 创建或维护官网仓库

本次 `portfolio` 已用于官网。直接打开 <https://github.com/kongshanman/portfolio>；以下创建步骤仅在该仓库尚不存在时执行。

1. 点击右上角 **＋ → New repository**。
2. **Owner** 选 `kongshanman`；**Repository name** 填 `portfolio`。
3. 描述填 `AetherCode Labs - developer tooling studio.`。
4. 选择 **Public**、开启 **Add README**，然后点击 **Create repository**。

### 新建 index.html

1. 复制物料 4 的完整原始 HTML，从 `<!doctype html>` 到最后的 `</html>`；不要把 Markdown 代码框标记一起复制。
2. 在 `portfolio` 的 **Code** 页点击 **Add file → Create new file**。
3. 文件名填 `index.html`，全部小写，放在根目录。不要填 `portfolio/index.html`，也不要变成 `index.html.txt`。
4. 将完整 HTML 粘贴到编辑框。
5. 点击 **Commit changes…**，填 `feat: add studio website`，选直接提交到 `main`，再点击弹窗中的 **Commit changes**。
6. 如果文件已经存在，点 `index.html` 的铅笔编辑并替换内容，不重复新建。

### 加入下载所需文件

网站的 README 下载按钮依赖真实文件。按 **Add file → Create new file** 依次添加：

| 文件名（完整输入） | 粘贴内容 |
| --- | --- |
| `materials/profile-README.md` | 物料 1 |
| `materials/ast-refactor-core-README.md` | 物料 2 |
| `materials/cli-testgen-README.md` | 物料 3 |
| `LICENSE` | 完整 MIT 许可证 |

输入文件名中的 `/` 会创建文件夹；无需另外找“新建文件夹”按钮。每个文件都点 **Commit changes…** 并在弹窗中再次保存。

最后用同样方式新建 `.nojekyll`（注意开头有一个点），编辑框填写 `Static site; Jekyll processing is disabled.` 并保存。GitHub 根据这个文件是否存在来关闭 Jekyll 处理，内容不影响作用；本套仓库已提供的空 `.nojekyll` 同样有效，已有就保留，无需重建。

网页新建文件、路径与保存步骤参考 [GitHub 官方新建文件说明](https://docs.github.com/en/repositories/working-with-files/managing-files/creating-new-files)。

## 4. 开启 GitHub Pages

1. 打开 `portfolio` 仓库，点击顶部齿轮旁的 **Settings / 设置**；这是仓库设置，不是头像菜单中的账号设置。
2. 在左侧 **Code and automation / 代码、规划和自动化** 下找到 **Pages / GitHub Pages**。
3. 在 **Build and deployment / 构建和部署** 区域，将 **Source / 来源** 设为 **Deploy from a branch / 从分支部署**。
4. 点击 **Branch / 分支** 下面的 **None / 无** 下拉框，选择 **main**。
5. 右侧文件夹选 **/ (root) / 根目录**。
6. 点击这行右边的 **Save / 保存**。保存后必须仍显示 `main` 与 `/ (root)`；仅看到“源已保存”而分支仍为 None，不代表启用成功。
7. **Custom domain / 自定义域** 留空。默认 `github.io` 网址已支持 HTTPS；不需要购买域名或启用 Enterprise 试用。

发布源配置参考 [GitHub 官方 Pages 配置说明](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。

### 找到并复制公网网址

1. 保存后等待部署；官方说明更改发布最多可能需要约十分钟。
2. 刷新当前 **Settings → Pages** 页面。
3. 在顶部找到 **Your site is live at… / 你的网站已发布于…** 和 **Visit site / 访问网站**。
4. 点击 **Visit site**，在打开的网页地址栏复制：<https://kongshanman.github.io/portfolio/>。
5. 也可点击仓库顶部 **Actions**，打开最新的 **pages build and deployment**。`build` 和 `deploy` 成功后再访问网站；绿色状态证明部署任务成功，页面实际效果仍需打开检查。

查看网址和发布时间参考 [GitHub 官方建站说明](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)。

## 5. 最后逐项检查

- [ ] 个人主页展示 AetherCode Labs 的 Bio、Mission、徽章和 Tech Stack。
- [ ] 两个项目位于两个独立公开仓库，仓库名准确，README 与 LICENSE 完整。
- [ ] 官网显示工作室名称、愿景、两张项目卡片和规格说明。
- [ ] 首页 Projects、Approach、Specifications 能滚动到对应位置。
- [ ] 两个项目详情可展开与收起；代码和参数表没有缺字。
- [ ] 两个项目仓库链接、三个 README 下载入口、MIT License 链接均能打开。
- [ ] 缩窄浏览器窗口检查排版；长代码允许在代码框内横向滚动，正文不应整体越界。
- [ ] 用未登录 GitHub 的浏览器窗口打开官网，确认它是公开地址。

项目当前是设计文档阶段。英文物料保留了这个真实状态：Node.js/Python 徽章表达技术计划，Build 徽章不表示工具测试已通过，示例不声称为已发布 API。网站和 README 是技术展示资料，不替代具体平台要求的审核证据。

## 6. 常见页面和对应操作

| 看到的情况 | 下一步 |
| --- | --- |
| Pages 分支是 None / 无 | 选 `main`、`/ (root)`，再 Save |
| 分支菜单没有 main | 回到 Code，确认 README 已提交；仓库不能是空仓库，然后刷新 Pages |
| 官网 404 | 检查 URL 包含 `/portfolio/`、根目录有 `index.html`、Actions 部署成功；刚发布先等待 |
| 官网仍是旧版 | 确认新的提交已部署成功，再刷新页面；不需要重新创建仓库 |
| 下载按钮 404 | 检查 `materials/` 下三个文件名与大小写，确保它们已经提交 |
| 看不到铅笔或 Settings | 确认登录 `kongshanman` 且进入自己的仓库 |
| 个人主页没显示 README | 仓库名须为 `kongshanman`、Public、根目录 README.md 非空 |

## 7. 由当前聊天连接代为写入时

手动网页编辑不需要任何 Connector。如果由本次聊天连接上传文件，新建仓库后需要在 [已安装的 GitHub 应用](https://github.com/settings/installations) 中找到 **ChatGPT Codex Connector → Configure / 配置**，保持 **Only select repositories / 仅选定仓库**，加入本次四个仓库并保存。保留原已选仓库，不改成所有仓库，也不修改其他应用。

本次四个仓库为：`kongshanman`、`ast-refactor-core`、`cli-testgen`、`portfolio`。应用授权完成不会自动创建仓库，也不会自动开启 Pages。
