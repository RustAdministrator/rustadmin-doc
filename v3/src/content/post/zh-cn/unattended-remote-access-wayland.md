---
publishDate: 2026-08-14T10:00:00Z
lang: 'zh-cn'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: '在 Wayland 上使用 RustDesk 实现无人值守远程访问'
excerpt: 'RustDesk 现已支持在 Wayland 上实现真正的无人值守远程访问，并支持多显示器。欢迎试用面向 x86_64 Debian/Ubuntu 系系统的预览版。'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: '发布'
tags: ['RustDesk', 'Wayland', 'Linux', '无人值守访问']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-zh-cn"

metadata:
  description: 'RustDesk 为 Wayland 带来真正的无人值守远程访问，并支持多显示器。面向 x86_64 Debian/Ubuntu 系系统的预览版现已发布。'
  keywords: 'RustDesk Wayland, Wayland 无人值守访问, Wayland 远程桌面, Linux 远程桌面 Wayland, RustDesk Linux, 无人值守远程访问'
---

Wayland 支持一直是 Linux 远程桌面中较难解决的部分之一。

RustDesk 现在可以在 Wayland 上提供**真正的无人值守访问**，无需远程电脑旁有人为每次会话进行批准。**同时也支持多显示器。**

完成初始设置后，即使远程电脑旁没有人，你也可以随时连接——包括重启后的**登录界面**。

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">在 X 上观看演示视频</a></blockquote>
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

目前，我们以独立预览版的形式发布该功能，适用于 **x86_64 的 Debian/Ubuntu 系系统**：

**[下载 Wayland 无人值守访问版本](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

多款主流远程桌面产品对 Wayland 的支持仍然有限。AnyDesk 目前在 Linux 上作为被控端仍需要 Xorg，而 TeamViewer 对常见桌面环境的 Wayland 支持仍被描述为实验性功能。

在将其设为默认方式之前，我们希望获得更多真实环境的测试反馈。

待实现稳定后，我们计划将 Wayland 无人值守访问带到更多 Linux 发行版，包括 **Fedora 和 Arch Linux**，并最终将其纳入 RustDesk 的标准发行版本。

如果你在使用 Wayland，尤其是多显示器环境，欢迎试用这个预览版，并告诉我们哪些功能正常、哪些还有问题。

## 相关阅读

- [RustDesk for Linux](/zh-cn/blog/rustdesk-for-linux-zh-cn)
- [RustDesk 无人值守访问](/zh-cn/blog/rustdesk-unattended-access-setup-zh-cn)
- [RustDesk 对比 AnyDesk](/zh-cn/blog/rustdesk-vs-anydesk-zh-cn)
- [RustDesk 对比 TeamViewer](/zh-cn/blog/rustdesk-vs-teamviewer-zh-cn)
