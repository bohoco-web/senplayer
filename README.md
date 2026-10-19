# SenPlayer 订阅备份（GitHub Pages）

腾讯云 COS 欠费会自动停服（2026-10-19 就停过一次），这里是同一批片单的**免费备用地址**。
文件内容与 COS 上完全一致，只是换了托管位置。

## 订阅地址

见 `index.html`，或直接访问：
`https://<用户名>.github.io/senplayer/`

## 文件说明

| 文件 | 内容 |
|---|---|
| `iptv-cn.m3u` | 中国大陆频道全量（含 A/B/C 画质等级标记） |
| `iptv-hmt.m3u` | 港澳台频道 |
| `iptv-cctv.m3u` / `iptv-satellite.m3u` / `iptv-province.m3u` / `iptv-city.m3u` | 按类别拆分的分册 |
| `iptv-intl.m3u` / `iptv-intl-ok.m3u` | 国际频道（全量 / 测活后） |
| `iptv-daino.m3u` / `iptv-daino-raw.m3u` | 外部订阅（分级版 / 原始备份） |
| `vidhub*.m3u` | SenPlayer 影视片单（全量 + 电影/剧集/综艺/动漫） |

## 怎么更新

```bash
cd ~/senplayer-pages && ./publish_pages.sh
```

脚本会从 `~/iptv-cn/out`、`~/iptv-intl/out`、`~/vidhub-m3u/out` 拉最新文件，
和仓库里的比对，**有变化才提交**，然后推送到 GitHub。

## 注意

GitHub 对版权投诉敏感，仓库被 DMCA 下架会整个消失。
所以 COS 那份别停，两边互为备份。
