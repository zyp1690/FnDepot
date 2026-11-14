# 火舞应用源 · 飞牛 fnOS 第三方应用源（FnDepot V2）

这里是我（火舞狂沙）自己维护的飞牛 fnOS 应用源，根目录的 `fnpack.json` 就是一份 **FnDepot V2 规范**的索引，可以直接当外部应用源添加。

## 添加方式

在 FnDepot 的「设置 → 应用源设置 → 添加应用源」中填：

```text
https://github.com/zyp1690/FnDepot
```

JSON 直链（方式二）：

```text
https://raw.githubusercontent.com/zyp1690/FnDepot/main/fnpack.json
```

> FnDepot 客户端需 ≥ 0.0.7 才支持 V2 源。

## 应用列表

| 应用 | 名称 | 版本 | 架构 | 说明 |
| --- | --- | --- | --- | --- |
| `ysplive` | ysplive 央视频直播 | 1.1.5 | all | 原生 FPK，免 Docker；央视频直播网页端，三栏界面 + 真节目单 + 全屏播放 + 选台浮层，支持 IPv4/IPv6，频道地址可编辑，另输出 M3U 订阅 |
| `duanju` | 火舞短剧 | 1.0.5 | x86 | 一站式短剧聚合播放器，内置 Node.js 运行时 |
| `iptv-api` | IPTV直播源自动更新平台 | 1.7.3 | x86 | 全自动采集、筛选、测速、生成直播源 |
| `nas-music` | NAS音乐播放器 | 1.0.0 | x86 | Node.js 音乐服务器，本地音乐管理 + 在线搜索 |
| `kerkerker` | 壳儿 Kerkerker | 1.0.0 | x86 | 影视聚合平台，TikTok 式刷片体验 |
| `php-epg` | php-epg IPTV 工具箱 | 2026.01.26 | x86 | EPG / 直播源 / 台标管理，兼容 DIYP、XMLTV |
| `php-runtime` | 轻量PHP管理器 | 2025.12.31 | x86 | 极简 PHP 环境管理，支持多版本切换 |

每个应用的 FPK、图标与 README 都在同名目录里；`ysplive` 的安装包与源码放在独立仓库 <https://github.com/zyp1690/ysplive>，索引里用绝对 URL 指向。

## 目录结构

```text
FnDepot/
├── fnpack.json                 # FnDepot V2 索引（客户端固定读这个文件名）
├── .github/
│   ├── fnpack-source.json      # 索引来源声明（url + sha256）
│   └── workflows/sync-fnpack.yml   # 拉取→校验→写入 fnpack.json
├── duanju/  iptv-api/  nas-music/  kerkerker/  php-epg/  php-runtime/
│   ├── ICON.PNG
│   ├── README.md
│   └── <app>.fpk
```

## 维护说明

- 新增/修改应用时，不要直接改 `fnpack.json`：把新索引上传后更新 `.github/fnpack-source.json` 的 `url` 与 `sha256`，推送到 `main` 后由 Actions 校验并写入（非法分类、platform、run_as、install_type 会直接让工作流失败，不会污染线上）。
- 发新版请用新版本号 + 新的 `download_url` / `size` / `sha256`，不要静默替换同版本同名 FPK。

## 致谢与版权

各应用版权归各自上游作者所有，本仓库只做 fnOS 打包适配与索引分发；每个应用目录下的 `README.md` 保留了上游说明。
