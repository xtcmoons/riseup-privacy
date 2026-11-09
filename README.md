# 该休息啦（RiseUp）隐私政策

本仓库包含 macOS 应用「该休息啦」（RiseUp）的隐私政策页面，以单个静态网页的形式发布。页面没有构建步骤，也不依赖任何框架或外部资源。

## 项目介绍

「该休息啦」是一款 macOS 应用，本仓库只存放它的隐私政策页面，不包含应用本身的源代码。

页面以中文说明应用如何处理用户信息，当前生效日期为 2026 年 10 月 9 日，主要内容包括：

- 应用不收集、不传输、不分享任何个人信息；
- 提醒间隔、休息时长等所有设置仅保存在本机（用户偏好存储），不会离开设备；
- 应用不包含广告、数据分析或第三方数据收集组件，自身不发起网络连接；
- 应用不要求访问通讯录、照片、位置、麦克风、摄像头等设备上的其他数据；
- 开启「登录时启动」时，应用通过 macOS 的登录项机制（SMAppService）向系统注册，可在「系统设置 → 通用 → 登录项」中移除；
- 由于不收集信息，应用同样不会收集儿童的信息，适合所有年龄段使用；
- 政策如有变更，会更新页面并修订生效日期。

页面还提供联系邮箱 [xtcmoon@yeah.net](mailto:xtcmoon@yeah.net)，页脚注明开发者为 XTCm。页面声明了 `noindex`，不供搜索引擎收录。

该页面通过 GitHub Pages 发布，可直接访问：<https://xtcmoons.github.io/riseup-privacy/>

## 本地查看

页面是纯静态 HTML，无需安装依赖或执行构建。克隆仓库后，任选一种方式查看。

### 方式一：直接打开文件

在文件管理器中双击 `index.html`，或用浏览器打开它。也可以在终端中执行：

```bash
git clone https://github.com/xtcmoons/riseup-privacy.git
cd riseup-privacy
open index.html   # macOS
# xdg-open index.html   # Linux
# start index.html      # Windows
```

### 方式二：启动本地静态服务器

这种方式更接近通过网址访问页面的效果：

```bash
git clone https://github.com/xtcmoons/riseup-privacy.git
cd riseup-privacy
python3 -m http.server 8000
```

然后在浏览器中打开 <http://localhost:8000/>（服务器会自动返回目录下的 `index.html`），按 `Ctrl+C` 停止。

## 文件说明

| 文件 | 说明 |
| --- | --- |
| `README.md` | 本说明文档，介绍项目用途、本地查看方式和仓库中的主要文件。 |
| `index.html` | 隐私政策页面本身，也是仓库中唯一的网页文件；正文、内联样式和浅色/深色配色都在这一个文件里，没有外部依赖。 |

仓库没有 `package.json`、构建脚本或图片资源，修改 `index.html` 后刷新浏览器即可看到变化。
