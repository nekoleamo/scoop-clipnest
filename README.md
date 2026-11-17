# scoop-clipnest

clipnest 的 Scoop bucket（Windows）。

```powershell
scoop bucket add clipnest https://github.com/nekoleamo/scoop-clipnest
scoop install clipnest
scoop update clipnest          # 升级
scoop uninstall clipnest       # 卸载（数据在 %APPDATA%\clipnest，不会自动删）
```

国内网络用 Gitee 镜像 bucket（manifest 里的下载地址指向 Gitee 附件）：

```powershell
scoop bucket add clipnest https://gitee.com/null_593_5354/scoop-clipnest
```

或者直接跑一键安装脚本（自动选 GitHub / Gitee）：

```powershell
irm https://gitee.com/null_593_5354/clipnest/raw/main/install.ps1 | iex
```

## 说明

- 装的是 portable exe，不加 PATH，只在开始菜单建一个快捷方式（托盘应用，双击即可）
- 未签名：Scoop 的下载不带 Mark-of-the-Web，所以不会弹 SmartScreen
- `bucket/clipnest.json` 由主仓库的 `tools/release-go.sh` 生成；维护时可用 `scoop checkver clipnest -u` 自动追版本

上游：[nekoleamo/clipnest](https://github.com/nekoleamo/clipnest)
