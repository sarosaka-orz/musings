---
title: "購入 Zephyrus 之後的體驗"
date: 2026-07-19
tags: ["科技","Linux"]
excerpt: "新筆電和新麻煩。"
---

## 新筆電

由於得了個野雞獎，直接獲得了一臺新筆電。當然是在賣掉 M4 Pro 的情況下才得到的。不過也不錯了，在這貼一下：

- Model: ASUS ROG Zephyrus G16 (2025)
- CPU: AMD Ryzen AI 7 H 350 w/ Radeon 860M
- dGPU: NVIDIA RTX 5060 Laptop

其他的懶得打，總之 32G 內存給我用爽了。全鋁 CNC Unibody 我只能說質感不弱於 MacBook，但是整體設計方面和觸控板的硬件還是沒有 Mac 好。（其實我感覺再疊這個價格就要起飛了）

風扇的聲音會明顯比 Strix 系列要小很多，在日常使用的情況下是基本靜音的。基準頻率只有 2 Ghz 的 Ryzen AI 也沒弱到哪去，日常即使是開 Quiet 也可以很快的做出響應。

電池續航嘛，那肯定是沒辦法的事情了。這一塊，x86 是不太可能追上 ARM 的，除非把性能扔掉。沒怎麼做 tuning 的情況下大約 7 個小時，算不錯了。如果做一點 tuning 可以有 11-12 小時，不過還是沒有 Mac 什麼都不做 16 小時強。

## 新麻煩

衆所周知 NVIDIA 這一塊在 Linux 上就沒輕鬆過——Hyprland各種閃就對了，插核顯屁問題都沒。開 Plasma 就不閃了……然而我不可能再回去用 floating 了。tiling 誰用誰知道。

修了一天最後想通了。開發組也沒爲 NVIDIA 提供官方支持，基本也就是能用就行，不能用我也不給你修。與其回 floating 我更願意把線在重啓的時候重新接一下，插到核顯上就沒問題了。

一開始真的是各種問題， Windows 外接也有問題。一度懷疑真的是買到通病機型，結果發現只是線材問題（有待確認），總之現在確定是 Hyprland 問題，人家不修我也沒辦法。實在不行就 WSL 唄，反正我現在覺得工具就是工具，哪個 OS 順手就好，沒別的區別。

## 結語
如果 MacBook 可以換用自己的 compositor，那麼我將成爲 Apple 最忠實的擁護者。

Mac 的質感和外圍硬件我就給五個字，「誰用誰知道」。

tiling WM 同上，建議各位趁早嘗試 GlazeWM / yabai / Hyprland.