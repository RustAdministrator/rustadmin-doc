---
publishDate: 2026-08-14T10:00:00Z
lang: 'ja'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: 'RustDesk による Wayland での無人リモートアクセス'
excerpt: 'RustDesk は Wayland 上で真の無人リモートアクセスを実現しました。マルチモニター構成にも対応しています。x86_64 の Debian/Ubuntu 系システム向けプレビュービルドをぜひお試しください。'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: 'リリース'
tags: ['RustDesk', 'Wayland', 'Linux', '無人アクセス']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-ja"

metadata:
  description: 'RustDesk が Wayland に真の無人リモートアクセスをもたらします。マルチモニターにも対応。x86_64 の Debian/Ubuntu 系システム向けプレビュービルドを公開中です。'
  keywords: 'RustDesk Wayland, Wayland 無人アクセス, Wayland リモートデスクトップ, Linux リモートデスクトップ Wayland, RustDesk Linux, 無人リモートアクセス'
---

Wayland への対応は、Linux リモートデスクトップの中でも特に難しい課題のひとつでした。

RustDesk は、リモート側のマシンで毎回セッションを承認してもらう必要のない、**Wayland 上での真の無人アクセス**を提供できるようになりました。**マルチモニター構成にも対応しています。**

初回のセットアップを済ませれば、リモート側に誰もいなくても接続できます。再起動後の**ログイン画面**からでも大丈夫です。

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">X でデモ動画を見る</a></blockquote>
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

現時点では、**x86_64 の Debian/Ubuntu 系システム**向けの独立したプレビュービルドとして公開しています。

**[Wayland 無人アクセス版をダウンロード](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

主要なリモートデスクトップ製品でも、Wayland 対応はまだ限定的です。AnyDesk は現在、Linux への着信セッションに Xorg を必要としており、TeamViewer も一般的なデスクトップ環境での Wayland 対応を実験的機能と位置付けています。

デフォルトにする前に、より多くの実環境でのテストを重ねたいと考えています。

実装が安定した段階で、**Fedora や Arch Linux** をはじめとするより多くの Linux ディストリビューションへ Wayland 無人アクセスを展開し、最終的には RustDesk の標準リリースに組み込む予定です。

Wayland をお使いの方、特にマルチモニター環境の方は、ぜひプレビュービルドを試して、うまく動く点・動かない点を教えてください。

## 関連記事

- [RustDesk for Linux](/ja/blog/rustdesk-for-linux-ja)
- [RustDesk無人アクセス設定ガイド](/ja/blog/rustdesk-unattended-access-setup-ja)
- [RustDesk vs AnyDesk](/ja/blog/rustdesk-vs-anydesk-ja)
- [RustDesk vs TeamViewer](/ja/blog/rustdesk-vs-teamviewer-ja)
