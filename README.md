# 小Bi的碎碎念（网页版 · 可部署到 GitHub Pages）

一个纯前端、零后端的个人日记本：新增日记、查看/编辑过往、记录体重折线图、7 套主题、导出/导入备份。数据全部存在浏览器 `localStorage`。

## 这个文件夹里有什么（上传到 GitHub 就这些）

| 文件 | 作用 |
| --- | --- |
| `index.html` | 全部代码（HTML+CSS+JS 内联），双击即可本地打开，也是网站首页 |
| `manifest.webmanifest` | 让手机「添加到主屏幕」时像 App 一样有图标、全屏打开 |
| `icon.svg` | 主屏幕图标 |
| `.nojekyll` | 告诉 GitHub Pages 不要走 Jekyll 处理，避免误删文件 |
| `README.md` | 本说明 |

> 只需 `index.html` 就能跑；其余文件是为了「手机端体验更好」。

## 方式一：最简上传（网页拖拽，不用命令行）

1. 打开 https://github.com ，登录 → 右上角 **New** 新建仓库，名字随意（如 `suisui`），**Public** 勾选，其他默认。
2. 建好后进入仓库，点 **Add file → Upload files**，把本文件夹里**全部文件**拖进去，写个提交说明，点 **Commit changes**。
3. 仓库页面 → **Settings → Pages → Build and deployment**，Source 选 **Deploy from a branch**，Branch 选 **main**（或 **master**），目录 **/ (root)**，保存。
4. 等约 1 分钟，访问 `https://你的用户名.github.io/仓库名/` 即可。

## 方式二：用 git 命令（已在本文件夹初始化好仓库，只差你加上远程）

```bash
cd deploy
git remote add origin https://github.com/你的用户名/仓库名.git
git branch -M main
git push -u origin main
```
推送后同样到 Settings → Pages 开启 Pages（选 main / root）。

## 手机上使用

- 用手机浏览器打开上面的 GitHub Pages 网址。
- **iOS（Safari）**：点底部「分享」→「添加到主屏幕」，之后像 App 一样从桌面打开，全屏无地址栏。
- **Android（Chrome）**：点「⋮」菜单 →「安装应用 / 添加到主屏幕」。
- 主题、标题、签名在右上角头像 → 设置里改。

## ⚠️ 重要：数据只存在这台设备的浏览器里

- 这是纯静态站点，**没有服务器、没有账号、没有云同步**。日记数据存在你打开网站的那个浏览器中。
- 换手机 / 换浏览器 / 清缓存 / 无痕模式 → **数据看不到，且无法找回**。
- 所以请养成习惯：**设置 → 导出备份**（下载一个 JSON），换设备时用「导入备份」恢复。
- 多设备「同步」的做法：在一台设备导出，把 JSON 传到另一台，再导入（或直接把同一个 JSON 存到网盘）。

数据无价，勤备份。
