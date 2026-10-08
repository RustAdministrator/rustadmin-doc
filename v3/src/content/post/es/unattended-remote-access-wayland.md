---
publishDate: 2026-08-14T10:00:00Z
lang: 'es'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: 'Acceso remoto desatendido en Wayland con RustDesk'
excerpt: 'RustDesk ahora ofrece verdadero acceso remoto desatendido en Wayland, incluidas las configuraciones multimonitor. Prueba la versión preliminar para sistemas x86_64 basados en Debian/Ubuntu.'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: 'Lanzamiento'
tags: ['RustDesk', 'Wayland', 'Linux', 'acceso desatendido']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-es"

metadata:
  description: 'RustDesk lleva el verdadero acceso remoto desatendido a Wayland, con soporte multimonitor. Ya está disponible una versión preliminar para sistemas x86_64 basados en Debian/Ubuntu.'
  keywords: 'RustDesk Wayland, acceso desatendido Wayland, escritorio remoto Wayland, escritorio remoto Linux Wayland, RustDesk Linux, acceso remoto desatendido'
---

La compatibilidad con Wayland ha sido una de las partes más difíciles del escritorio remoto en Linux.

RustDesk ahora puede ofrecer **verdadero acceso desatendido en Wayland**, sin necesidad de que alguien en la máquina remota apruebe cada sesión. **También se admiten configuraciones multimonitor.**

Tras la configuración inicial, puedes conectarte aunque no haya nadie en la máquina remota, incluso desde la **pantalla de inicio de sesión** tras un reinicio.

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">Ver el vídeo de demostración en X</a></blockquote>
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

Por ahora, lo publicamos como una versión preliminar independiente para **sistemas x86_64 basados en Debian/Ubuntu**:

**[Descargar la versión de Wayland con acceso desatendido](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

La compatibilidad con Wayland sigue siendo limitada en varios de los principales productos de escritorio remoto. AnyDesk actualmente requiere Xorg para las sesiones entrantes en Linux, mientras que TeamViewer aún describe su compatibilidad con Wayland como experimental para los entornos de escritorio habituales.

Queremos recopilar más pruebas en entornos reales antes de convertirlo en el comportamiento predeterminado.

Cuando la implementación sea estable, planeamos llevar el acceso desatendido en Wayland a más distribuciones de Linux, incluidas **Fedora y Arch Linux**, y finalmente incluirlo en las versiones estándar de RustDesk.

Si usas Wayland, especialmente con varios monitores, prueba la versión preliminar y cuéntanos qué funciona… y qué no.

## Lecturas relacionadas

- [RustDesk para Linux](/es/blog/rustdesk-para-linux-el-escritorio-remoto-de-codigo-abierto)
- [Acceso desatendido en RustDesk](/es/blog/acceso-desatendido-en-rustdesk-guia-de-configuracion)
- [RustDesk vs AnyDesk](/es/blog/rustdesk-vs-anydesk-escritorio-remoto-autoalojado-y-de-codigo-abierto)
- [RustDesk vs TeamViewer](/es/blog/rustdesk-vs-teamviewer-la-alternativa-autoalojada)
