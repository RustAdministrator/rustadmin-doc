---
publishDate: 2026-08-14T10:00:00Z
lang: 'it'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: 'Accesso remoto non presidiato su Wayland con RustDesk'
excerpt: 'RustDesk ora offre un vero accesso remoto non presidiato su Wayland, incluse le configurazioni multi-monitor. Prova la build di anteprima per i sistemi x86_64 basati su Debian/Ubuntu.'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: 'Rilascio'
tags: ['RustDesk', 'Wayland', 'Linux', 'accesso non presidiato']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-it"

metadata:
  description: "RustDesk porta il vero accesso remoto non presidiato su Wayland, con supporto multi-monitor. È ora disponibile una build di anteprima per i sistemi x86_64 basati su Debian/Ubuntu."
  keywords: 'RustDesk Wayland, accesso non presidiato Wayland, desktop remoto Wayland, desktop remoto Linux Wayland, RustDesk Linux, accesso remoto non presidiato'
---

Il supporto a Wayland è sempre stato uno degli aspetti più difficili del desktop remoto su Linux.

RustDesk ora può offrire un **vero accesso non presidiato su Wayland**, senza che qualcuno sulla macchina remota debba approvare ogni sessione. **Sono supportate anche le configurazioni multi-monitor.**

Dopo la configurazione iniziale, puoi collegarti anche quando non c'è nessuno alla macchina remota — perfino dalla **schermata di accesso** dopo un riavvio.

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">Guarda il video dimostrativo su X</a></blockquote>
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

Per ora la rilasciamo come build di anteprima separata per i **sistemi x86_64 basati su Debian/Ubuntu**:

**[Scarica la build Wayland con accesso non presidiato](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

Il supporto a Wayland è ancora limitato in diversi importanti prodotti di desktop remoto. AnyDesk attualmente richiede Xorg per le sessioni Linux in ingresso, mentre TeamViewer descrive ancora il supporto a Wayland come sperimentale per gli ambienti desktop più comuni.

Vorremmo raccogliere più test in condizioni reali prima di renderlo il comportamento predefinito.

Una volta che l'implementazione sarà stabile, prevediamo di portare l'accesso non presidiato su Wayland a più distribuzioni Linux, tra cui **Fedora e Arch Linux**, e infine di includerlo nelle versioni standard di RustDesk.

Se usi Wayland, soprattutto con più monitor, prova la build di anteprima e facci sapere cosa funziona — e cosa no.

## Approfondimenti correlati

- [RustDesk per Linux](/it/blog/rustdesk-per-linux-il-desktop-remoto-open-source)
- [Accesso non presidiato con RustDesk](/it/blog/accesso-non-presidiato-con-rustdesk-guida-alla-configurazione)
- [RustDesk vs AnyDesk](/it/blog/rustdesk-vs-anydesk-desktop-remoto-self-hosted-e-open-source)
- [RustDesk vs TeamViewer](/it/blog/rustdesk-vs-teamviewer-lalternativa-self-hosted)
