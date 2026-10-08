---
publishDate: 2026-08-14T10:00:00Z
lang: 'pt'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: 'Acesso remoto não assistido no Wayland com RustDesk'
excerpt: 'O RustDesk agora oferece verdadeiro acesso remoto não assistido no Wayland, incluindo configurações com vários monitores. Experimente a versão de pré-visualização para sistemas x86_64 baseados em Debian/Ubuntu.'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: 'Lançamento'
tags: ['RustDesk', 'Wayland', 'Linux', 'acesso não assistido']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-pt"

metadata:
  description: 'O RustDesk traz verdadeiro acesso remoto não assistido para o Wayland, com suporte a vários monitores. Uma versão de pré-visualização para sistemas x86_64 baseados em Debian/Ubuntu já está disponível.'
  keywords: 'RustDesk Wayland, acesso não assistido Wayland, área de trabalho remota Wayland, área de trabalho remota Linux Wayland, RustDesk Linux, acesso remoto não assistido'
---

O suporte ao Wayland tem sido uma das partes mais difíceis da área de trabalho remota no Linux.

O RustDesk agora pode oferecer **verdadeiro acesso não assistido no Wayland**, sem exigir que alguém na máquina remota aprove cada sessão. **Configurações com vários monitores também são suportadas.**

Após a configuração inicial, você pode se conectar mesmo quando não há ninguém na máquina remota — inclusive a partir da **tela de login** após uma reinicialização.

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">Assista ao vídeo de demonstração no X</a></blockquote>
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

Por enquanto, estamos lançando isso como uma versão de pré-visualização separada para **sistemas x86_64 baseados em Debian/Ubuntu**:

**[Baixar a versão Wayland com acesso não assistido](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

O suporte ao Wayland ainda é limitado em vários dos principais produtos de área de trabalho remota. O AnyDesk atualmente exige Xorg para sessões recebidas no Linux, enquanto o TeamViewer ainda descreve o suporte ao Wayland como experimental para os ambientes de desktop mais comuns.

Gostaríamos de reunir mais testes em condições reais antes de torná-lo o padrão.

Quando a implementação estiver estável, planejamos levar o acesso não assistido no Wayland a mais distribuições Linux, incluindo **Fedora e Arch Linux**, e, por fim, incluí-lo nas versões padrão do RustDesk.

Se você usa Wayland, especialmente com vários monitores, experimente a versão de pré-visualização e conte para nós o que funciona — e o que não funciona.

## Leituras relacionadas

- [RustDesk para Linux](/pt/blog/rustdesk-para-linux-o-desktop-remoto-de-codigo-aberto)
- [Acesso Não Assistido do RustDesk](/pt/blog/acesso-nao-assistido-do-rustdesk-guia-de-configuracao)
- [RustDesk vs AnyDesk](/pt/blog/rustdesk-vs-anydesk-area-de-trabalho-remota-auto-hospedada-e-de-codigo)
- [RustDesk vs TeamViewer](/pt/blog/rustdesk-vs-teamviewer-a-alternativa-auto-hospedada)
