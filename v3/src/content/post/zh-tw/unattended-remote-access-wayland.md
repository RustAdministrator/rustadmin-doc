---
publishDate: 2026-08-14T10:00:00Z
lang: 'zh-tw'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: '在 Wayland 上使用 RustDesk 實現無人值守遠端存取'
excerpt: 'RustDesk 現已支援在 Wayland 上實現真正的無人值守遠端存取，並支援多螢幕。歡迎試用適用於 x86_64 Debian/Ubuntu 系系統的預覽版。'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: '發布'
tags: ['RustDesk', 'Wayland', 'Linux', '無人值守存取']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-zh-tw"

metadata:
  description: 'RustDesk 為 Wayland 帶來真正的無人值守遠端存取，並支援多螢幕。適用於 x86_64 Debian/Ubuntu 系系統的預覽版現已發布。'
  keywords: 'RustDesk Wayland, Wayland 無人值守存取, Wayland 遠端桌面, Linux 遠端桌面 Wayland, RustDesk Linux, 無人值守遠端存取'
---

Wayland 支援一直是 Linux 遠端桌面中較難解決的部分之一。

RustDesk 現在可以在 Wayland 上提供**真正的無人值守存取**，無需遠端電腦旁有人為每次連線進行核准。**同時也支援多螢幕。**

完成初始設定後，即使遠端電腦旁沒有人，你也可以隨時連線——包括重新開機後的**登入畫面**。

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">在 X 上觀看示範影片</a></blockquote>
</div>
<script data-astro-rerun>
(function () {
  if (window.twttr && window.twttr.widgets) {
    window.twttr.widgets.load();
  } else if (!document.getElementById('twitter-wjs')) {
    var s = document.createElement('script');
    s.id = 'twitter-wjs';
    s.async = true;
    s.src = 'https://platform.twitter.com/widgets.js';
    document.head.appendChild(s);
  }
})();
</script>

目前，我們以獨立預覽版的形式發布此功能，適用於 **x86_64 的 Debian/Ubuntu 系系統**：

**[下載 Wayland 無人值守存取版本](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

多款主流遠端桌面產品對 Wayland 的支援仍然有限。AnyDesk 目前在 Linux 上作為受控端仍需要 Xorg，而 TeamViewer 對常見桌面環境的 Wayland 支援仍被描述為實驗性功能。

在將其設為預設方式之前，我們希望獲得更多真實環境的測試回饋。

待實作穩定後，我們計劃將 Wayland 無人值守存取帶到更多 Linux 發行版，包括 **Fedora 和 Arch Linux**，並最終將其納入 RustDesk 的標準發行版本。

如果你在使用 Wayland，尤其是多螢幕環境，歡迎試用這個預覽版，並告訴我們哪些功能正常、哪些還有問題。

## 延伸閱讀

- [RustDesk for Linux](/zh-tw/blog/rustdesk-for-linux-zh-tw)
- [RustDesk 無人值守存取](/zh-tw/blog/rustdesk-unattended-access-setup-zh-tw)
- [RustDesk vs AnyDesk](/zh-tw/blog/rustdesk-vs-anydesk-zh-tw)
- [RustDesk 對比 TeamViewer](/zh-tw/blog/rustdesk-vs-teamviewer-zh-tw)
