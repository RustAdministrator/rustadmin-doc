---
publishDate: 2026-08-14T10:00:00Z
lang: en
translationKey: unattended-remote-access-wayland
draft: false
title: 'Unattended Remote Access on Wayland with RustDesk'
excerpt: 'RustDesk now provides true unattended remote access on Wayland, including multi-monitor setups. Try the preview build for x86_64 Debian/Ubuntu-based systems.'
image: ~/assets/images/blog/unattended-remote-access-wayland-og.webp
category: Release
tags:
  - RustDesk
  - Wayland
  - Linux
  - unattended-access
author: RustDesk Team

metadata:
  description: 'RustDesk brings true unattended remote access to Wayland, with multi-monitor support. A preview build for x86_64 Debian/Ubuntu-based systems is available now.'
  keywords: 'RustDesk Wayland, Wayland unattended access, Wayland remote desktop, Linux remote desktop Wayland, RustDesk Linux, unattended remote access'
---

Wayland support has been one of the harder parts of Linux remote desktop.

RustDesk can now provide **true unattended access on Wayland**, without requiring someone at the remote machine to approve every session. **Multi-monitor setups are supported as well.**

After the initial setup, you can connect even when no one is at the remote machine — including from the **login screen** after a reboot.

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">Watch the demo video on X</a></blockquote>
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

For now, we are releasing this as a separate preview build for **x86_64 Debian/Ubuntu-based systems**:

**[Download the Wayland unattended access build](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

Wayland support is still limited in several major remote desktop products. AnyDesk currently requires Xorg for incoming Linux sessions, while TeamViewer still describes Wayland support as experimental for common desktop environments.

We would like to get more real-world testing before making this the default.

Once the implementation is stable, we plan to bring unattended Wayland access to more Linux distributions, including **Fedora and Arch Linux**, and eventually include it in the standard RustDesk releases.

If you use Wayland, especially with multiple monitors, please give the preview build a try and let us know what works—and what doesn't.

## Related reading

- [RustDesk for Linux](/blog/rustdesk-for-linux)
- [RustDesk Unattended Access](/blog/rustdesk-unattended-access-setup)
- [RustDesk vs AnyDesk](/blog/rustdesk-vs-anydesk)
- [RustDesk vs TeamViewer](/blog/rustdesk-vs-teamviewer)
