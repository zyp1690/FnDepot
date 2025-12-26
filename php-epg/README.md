📺 IPTV工具箱
IPTV Tool | Trendshift
GitHub Stars GitHub Forks GitHub Issues GitHub Pull Requests License Docker Pulls Image Size

IPTV 工具箱， Docker 部署，支持 EPG 管理、直播源管理、台标管理，兼容 DIYP/百川、 超级直播以及 xmltv 格式。

Tip

⚠️ 使用前请仔细阅读「管理页面」底部的「使用说明」

原贴：【IPTV工具箱】EPG节目单管理、直播源管理、台标管理

xmltv 用户使用方法：【一键生成】匹配 M3U 文件的 XML 节目单

直播源管理 使用方法：【IPTV工具箱】直播源管理使用说明

自定数据源 使用方法：【IPTV工具箱】自定义数据源（timetv、51livetv、diyp）

💻 主要功能
📡 多格式：支持返回 DIYP/百川、超级直播以及 xmltv 格式文件。

🐳 多架构：提供 amd64、arm64 和 armv7 架构的 Docker 镜像。

📦 小体积镜像：基于 Alpine 构建，压缩后仅 20 MB。

🗃️ 数据库管理：支持 SQLite 和 MySQL 数据库，内置 phpLiteAdmin 管理工具。

🖼️ 台标管理：支持台标模糊匹配，支持 tvbox 接口。

➰ 直播源管理：支持聚合 TXT/M3U 直播源、测速校验、直播源代理。

🔒 访问权限控制：支持设置 TOKEN 、User-Agent、IP 黑白名单。

⏱️ 缓存支持：集成 Memcached，支持 Redis。

🔄 频道匹配：支持繁体中文频道匹配、模糊匹配；支持频道别名、正则表达式。

⏳ 定时任务：支持定时更新数据。

📝 节目单生成：支持生成指定频道节目单并匹配 M3U 的 xmltv 格式文件。

🗂️ 兼容多种格式：支持不同标准格式的 XMLTV 文件，支持自定义数据源。

🛠️ 文件管理：集成 tinyfilemanager 文件管理器。

🌐 界面设置：包含简单易用的网页设置页面，便于操作和管理。

设置页面