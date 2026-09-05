---
title: Fcitx5 + ii 使用手冊
date: 2026-06-23
tags: ["科技","Linux","問題"]
excerpt: 關於在 Linux 上使用 Fcitx5 + ii 的一些修復經驗。
---

## Fcitx5 + ii 疑難解答

距離我正式改用基於 Quickshell 的 illogical-impulse 作爲主力環境已經有一點時間了，這段時間我也遇到了一些關於 Fcitx5 + ii 的問題，這裡總結一下我的經驗，希望能幫助到其他使用者。

對於 illogical-impulse:
可能在社羣中大家會更廣泛的稱其爲 end_4 dotfiles。

正常的安裝只需要按照官方文檔的指引進行即可，這裡不再贅述。許多 Linux 論壇也已經有了關於 Fcitx5 的安裝教程，這裡主要針對一些特殊的問題進行解答。

### 爲什麼只有開終端才能打中文？

我相信不止一位使用者其實碰見過這種問題，在 ii 環境下只有在後臺留置一個 kitty 才能用 fcitx5 打字，而在 Firefox 或者 LibreOffice 中卻無法使用。一關掉 kitty 就會沒辦法打字，具體來說是 `GTK_IM_MODULE` 和 D-Bus 啓動順序的原因。

在 ~/.config/hypr/custom/env.lua 中添加以下內容：

```lua
hl.env("QT_IM_MODULE", "fcitx")
hl.env("XMODIFIERS", "@im=fcitx")
hl.env("GLFW_IM_MODULE", "fcitx")
```

在 ~/.config/hypr/custom/execs.lua 中添加以下內容：

```lua
hl.on("hyprland.start", function()
	hl.exec_cmd("dbus-update-activation-environment --systemd --all")
	hl.exec_cmd("dbus-update-activation-environment --systemd WAYLAND_DISPLAY XDG_CURRENT_DESKTOP")
	hl.exec_cmd("fcitx5 -d --replace")
end)
```

而後 logout 並重新登入即可。