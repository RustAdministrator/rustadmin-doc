---
publishDate: 2026-08-14T10:00:00Z
lang: 'ar'
translationKey: 'unattended-remote-access-wayland'
draft: false
title: 'الوصول عن بُعد غير المراقب على Wayland باستخدام RustDesk'
excerpt: 'يوفّر RustDesk الآن وصولاً حقيقياً غير مراقب عن بُعد على Wayland، بما في ذلك دعم الشاشات المتعددة. جرّب الإصدار التجريبي لأنظمة x86_64 المبنية على Debian/Ubuntu.'
image: '~/assets/images/blog/unattended-remote-access-wayland-og.webp'
category: 'إصدار'
tags: ['RustDesk', 'Wayland', 'Linux', 'الوصول غير المراقب']
author: 'RustDesk Team'
slug: "unattended-remote-access-wayland-ar"

metadata:
  description: 'يجلب RustDesk الوصول الحقيقي غير المراقب عن بُعد إلى Wayland، مع دعم الشاشات المتعددة. الإصدار التجريبي لأنظمة x86_64 المبنية على Debian/Ubuntu متاح الآن.'
  keywords: 'RustDesk Wayland, الوصول غير المراقب Wayland, سطح المكتب البعيد Wayland, سطح المكتب البعيد لينكس Wayland, RustDesk لينكس, الوصول عن بعد غير المراقب'
---

لطالما كان دعم Wayland من أصعب جوانب سطح المكتب البعيد على لينكس.

يستطيع RustDesk الآن توفير **وصول حقيقي غير مراقب على Wayland**، دون الحاجة إلى وجود شخص عند الجهاز البعيد للموافقة على كل جلسة. **كما أن إعدادات الشاشات المتعددة مدعومة أيضاً.**

بعد الإعداد الأولي، يمكنك الاتصال حتى لو لم يكن هناك أحد عند الجهاز البعيد — بما في ذلك من **شاشة تسجيل الدخول** بعد إعادة التشغيل.

<div class="twitter-embed" style="display:flex;justify-content:center;">
<blockquote class="twitter-video" data-media-max-width="560"><a href="https://twitter.com/rustdesk/status/2087945266855026744">شاهد الفيديو التوضيحي على X</a></blockquote>
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

في الوقت الحالي، نُصدر هذه الميزة كإصدار تجريبي منفصل لأنظمة **x86_64 المبنية على Debian/Ubuntu**:

**[تنزيل إصدار Wayland للوصول غير المراقب](https://github.com/rustdesk/rustdesk/releases/download/nightly/rustdesk-unattended-wayland-1.4.9-x86_64.deb)**

لا يزال دعم Wayland محدوداً في العديد من منتجات سطح المكتب البعيد الرئيسية. يتطلب AnyDesk حالياً Xorg للجلسات الواردة على لينكس، بينما لا يزال TeamViewer يصف دعمه لـ Wayland بأنه تجريبي في بيئات سطح المكتب الشائعة.

نودّ الحصول على المزيد من الاختبارات في بيئات حقيقية قبل جعل هذا هو الوضع الافتراضي.

بمجرد استقرار التنفيذ، نخطط لجلب الوصول غير المراقب على Wayland إلى المزيد من توزيعات لينكس، بما في ذلك **Fedora و Arch Linux**، وإدراجه في النهاية ضمن إصدارات RustDesk القياسية.

إذا كنت تستخدم Wayland، وخصوصاً مع عدة شاشات، فجرّب الإصدار التجريبي وأخبرنا بما يعمل جيداً — وما لا يعمل.

## قراءات ذات صلة

- [RustDesk لنظام Linux](/ar/blog/rustdesk-for-linux-ar)
- [الوصول غير المراقب في RustDesk](/ar/blog/rustdesk-unattended-access-setup-ar)
- [RustDesk مقابل AnyDesk](/ar/blog/rustdesk-vs-anydesk-ar)
- [RustDesk مقابل TeamViewer](/ar/blog/rustdesk-vs-teamviewer-ar)
