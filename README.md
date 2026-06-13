# 自动化开发 - 个人作品集

一个面向自动化接单的个人作品集静态页面，适合自由职业者展示服务、案例和联系方式。

## 快速使用

1. **编辑个人信息**

   打开 `index.html`，搜索以下注释标记并替换为你自己的信息：

   | 搜索标记 | 替换内容 |
   |----------|----------|
   | `<!-- 换成你的邮箱 -->` | 你的联系邮箱 |
   | `<!-- 换成你的 GitHub -->` | GitHub 用户名链接 |

   关于我的段落中(`#about` 部分)，把默认的自我介绍改成你自己的。

2. **统计数据**

   `index.html` 底部 JS 中有三处数字：
   ```js
   animateCount(document.getElementById('statProjects'), 28);  // 改成你的项目数
   animateCount(document.getElementById('statClients'), 15);   // 改成你的客户数
   animateCount(document.getElementById('statRate'), 100, '%'); // 好评率
   ```

3. **项目案例**

   `#projects` 区域的三个卡片是示例，替换成你实际做过的项目。如果还没有项目，可以先留着做占位。

4. **联系表单**

   当前表单提交只是弹窗提示。你需要接入一个表单后端服务（推荐方案见下文）。

## 部署方案（免费）

### 方案一：GitHub Pages（推荐）

1. 在 GitHub 新建一个仓库，比如 `username/username.github.io` 或任意仓库名
2. 把 `index.html` 推上去
3. 进入仓库 Settings → Pages
4. Source 选 "Deploy from a branch"，分支选 `main`，目录选 `/ (root)`
5. 几分钟后就能在 `https://username.github.io` 访问

### 方案二：Vercel

1. 注册 [vercel.com](https://vercel.com)（支持 GitHub 登录）
2. 新建项目 → Import Git Repository → 选择包含 `index.html` 的仓库
3. Framework Preset 选 "Other"，构建命令留空
4. 部署成功后自动获得 `your-project.vercel.app` 域名

### 方案三：Netlify

1. 注册 [netlify.com](https://netlify.com)
2. 拖拽整个文件夹到 Netlify 部署页面，或关联 Git 仓库
3. 自动获得 `your-site.netlify.app` 域名

## 表单后端接入方案

| 方案 | 免费额度 | 接入难度 |
|------|---------|---------|
| [Formspree](https://formspree.io) | 每月 50 条 | 低，改表单 action 即可 |
| [Web3Forms](https://web3forms.com) | 每月 250 条 | 低 |
| 自己用 Vercel Functions 写一个 | 无限 | 需要写几行 Serverless 代码 |

## 域名

- 如果想用自己的域名（比如 `yourname.com`），可以在 Namecheap / 阿里云 / Cloudflare 买一个
- GitHub Pages / Vercel / Netlify 都支持绑定自定义域名
- Cloudflare 可以提供免费的 DNS 和 SSL

## 自定义

- **颜色**：修改 `:root` 中的 `--primary`、`--accent` 等 CSS 变量
- **品牌名**：顶部导航的 `AutoDev` 可以改成你自己的名字
- **技术栈**：`#about` 下面的技能卡片可以增删

