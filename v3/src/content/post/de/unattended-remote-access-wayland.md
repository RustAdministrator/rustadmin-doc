---
publishDate: 2026-08-14T10:00:00Z
lang: 'de'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: 'Unbeaufsichtigter Fernzugriff unter Wayland mit RustDesk'
excerpt: 'RustDesk bietet jetzt echten unbeaufsichtigten Fernzugriff unter Wayland, inklusive Multi-Monitor-Setups. Probieren Sie den Preview-Build für x86_64 Debian/Ubuntu-basierte Systeme aus.'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: 'Veröffentlichung'
tags: ['RustDesk', 'Wayland', 'Linux', 'unbeaufsichtigter Zugriff']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-de"

metadata:
  description: 'RustDesk bringt echten unbeaufsichtigten Fernzugriff auf Wayland, mit Multi-Monitor-Unterstützung. Ein Preview-Build für x86_64 Debian/Ubuntu-basierte Systeme ist jetzt verfügbar.'
  keywords: 'RustDesk Wayland, Wayland unbeaufsichtigter Zugriff, Wayland Remote-Desktop, Linux Remote-Desktop Wayland, RustDesk Linux, unbeaufsichtigter Fernzugriff'
---

Die Wayland-Unterstützung gehörte bisher zu den schwierigsten Aspekten des Linux-Remote-Desktops.

RustDesk kann jetzt **echten unbeaufsichtigten Zugriff unter Wayland** bieten – ohne dass jemand am entfernten Rechner jede Sitzung bestätigen muss. **Auch Multi-Monitor-Setups werden unterstützt.**

Nach der Ersteinrichtung können Sie sich verbinden, auch wenn niemand am entfernten Rechner ist – einschließlich des **Anmeldebildschirms** nach einem Neustart.

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">Demo-Video auf X ansehen</a></blockquote>
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

Vorerst veröffentlichen wir dies als separaten Preview-Build für **x86_64 Debian/Ubuntu-basierte Systeme**:

**[Wayland-Build für unbeaufsichtigten Zugriff herunterladen](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

Die Wayland-Unterstützung ist bei mehreren großen Remote-Desktop-Produkten noch eingeschränkt. AnyDesk benötigt für eingehende Linux-Sitzungen derzeit Xorg, während TeamViewer die Wayland-Unterstützung für gängige Desktop-Umgebungen weiterhin als experimentell bezeichnet.

Bevor wir dies zum Standard machen, möchten wir mehr Tests unter realen Bedingungen sammeln.

Sobald die Implementierung stabil ist, planen wir, den unbeaufsichtigten Wayland-Zugriff auf weitere Linux-Distributionen auszuweiten, darunter **Fedora und Arch Linux**, und ihn schließlich in die regulären RustDesk-Releases aufzunehmen.

Wenn Sie Wayland nutzen, insbesondere mit mehreren Monitoren, probieren Sie bitte den Preview-Build aus und teilen Sie uns mit, was funktioniert – und was nicht.

## Weiterführende Artikel

- [RustDesk für Linux](/de/blog/rustdesk-fur-linux-der-open-source-remote-desktop)
- [Unbeaufsichtigter Zugriff mit RustDesk](/de/blog/unbeaufsichtigter-zugriff-mit-rustdesk-einrichtungsanleitung)
- [RustDesk vs AnyDesk](/de/blog/rustdesk-vs-anydesk-selbst-gehostete-open-source-remotedesktop-software)
- [RustDesk vs. TeamViewer](/de/blog/rustdesk-vs-teamviewer-die-selbst-gehostete-alternative)
