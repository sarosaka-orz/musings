---
title: "關於一些 Ubuntu by Canonical 的事情。"
date: 2026-07-02
tags: ["科技","Linux"]
excerpt: "只有在今天正式用過 Ubuntu 做開發的，才會知道爲什麼。"
---

## 緣由

學校打算做具身智能的開發，于是購入了一臺 NVIDIA Jetson Orin NX 16GB, 衆所周知 JetPack 的 basic OS 是 Ubuntu。

## 問題

說真的，我一直認爲 Debian 系尤其是 Ubuntu by Canonical，是一個「穩定性」和「開箱即用」的代名詞，不僅僅是因爲 GUI 了大量的，原本需要在終端機一個個敲的命令，更是可以裝好直接開跑。如果你只把 Linux 用作工具，大可選擇 Ubuntu 作爲主力系統，好就好在它幾乎零配置，也不會今天一個滾動更新直接就把你丟進 emergency shell.

但是最近越來越多的人開始轉向 Fedora Linux.

我一直以爲只是 Debian 系的包太老了，因爲 Debian 系的 distro 就是這個樣子的，更新一個包需要進行成百上千次的測試，經歷很多的 testing channel，而 Fedora 的包相對會更新一點。

但我今天發現不是 **Debian** 的問題，而是 **Ubuntu** 的問題。

近年來 Ubuntu 越來越像一個被大公司控制的操作系統，也越來越臃腫，越來越像 Microsoft Windows. 尤其是在強制引入 Snap 包管理器以後。

Canonical 的說法是 Snap 更加安全，也更加便捷。但我看到的只是比 APT 長大約 3 倍的安裝時間，極慢的 App 啓動速度和更多的兼容性問題。私以爲，Flatpak 會比 Snap 更好。

其實引入 Snap 倒沒有什麼，但是把 APT 裏的包替換成 Snap 的過渡包，私認爲這就有點過分了。

強行引入一項被廣爲詬病的技術真的是爲了安全？私認爲 Canonical 的出發點是好的，但他們的行爲毀掉了 Ubuntu 這一個「開箱即用，穩定，易於使用」的 distro.

此致。另外我使用 Arch Linux.