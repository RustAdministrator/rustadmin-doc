---
publishDate: 2026-08-14T10:00:00Z
lang: 'fr'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: 'Accès à distance sans surveillance sous Wayland avec RustDesk'
excerpt: 'RustDesk offre désormais un véritable accès à distance sans surveillance sous Wayland, y compris pour les configurations multi-écrans. Essayez la version préliminaire pour les systèmes x86_64 basés sur Debian/Ubuntu.'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: 'Version'
tags: ['RustDesk', 'Wayland', 'Linux', 'accès sans surveillance']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-fr"

metadata:
  description: "RustDesk apporte un véritable accès à distance sans surveillance à Wayland, avec prise en charge du multi-écrans. Une version préliminaire pour les systèmes x86_64 basés sur Debian/Ubuntu est disponible dès maintenant."
  keywords: 'RustDesk Wayland, accès sans surveillance Wayland, bureau à distance Wayland, bureau à distance Linux Wayland, RustDesk Linux, accès à distance sans surveillance'
---

La prise en charge de Wayland a toujours été l'un des aspects les plus difficiles du bureau à distance sous Linux.

RustDesk peut désormais offrir un **véritable accès sans surveillance sous Wayland**, sans que quelqu'un doive approuver chaque session sur la machine distante. **Les configurations multi-écrans sont également prises en charge.**

Après la configuration initiale, vous pouvez vous connecter même si personne n'est devant la machine distante — y compris depuis l'**écran de connexion** après un redémarrage.

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">Voir la vidéo de démonstration sur X</a></blockquote>
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

Pour l'instant, nous publions cette fonctionnalité sous forme de version préliminaire distincte pour les **systèmes x86_64 basés sur Debian/Ubuntu** :

**[Télécharger la version Wayland avec accès sans surveillance](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

La prise en charge de Wayland reste limitée dans plusieurs grands produits de bureau à distance. AnyDesk exige actuellement Xorg pour les sessions Linux entrantes, tandis que TeamViewer décrit toujours sa prise en charge de Wayland comme expérimentale pour les environnements de bureau courants.

Nous souhaitons recueillir davantage de tests en conditions réelles avant d'en faire le comportement par défaut.

Une fois l'implémentation stabilisée, nous prévoyons d'étendre l'accès sans surveillance sous Wayland à d'autres distributions Linux, notamment **Fedora et Arch Linux**, puis de l'intégrer aux versions standard de RustDesk.

Si vous utilisez Wayland, en particulier avec plusieurs écrans, essayez la version préliminaire et dites-nous ce qui fonctionne — et ce qui ne fonctionne pas.

## Pour aller plus loin

- [RustDesk pour Linux](/fr/blog/rustdesk-pour-linux-le-bureau-a-distance-open-source)
- [Accès non surveillé RustDesk](/fr/blog/acces-non-surveille-rustdesk-guide-de-configuration)
- [RustDesk vs AnyDesk](/fr/blog/rustdesk-vs-anydesk-bureau-a-distance-open-source-et-auto-heberge)
- [RustDesk vs TeamViewer](/fr/blog/rustdesk-vs-teamviewer-lalternative-auto-hebergee)
