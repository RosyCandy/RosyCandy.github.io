---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

<div class="about-wrap">
  <div class="about-cloud">
    <i class="p p1"></i><i class="p p2"></i><i class="p p3"></i><i class="p p4"></i><i class="p p5"></i>
    <p>这里是 DuoDuo’s Daily，我是 Erieanna，这里是我记录日常生活、技术学习和音乐感悟的地方。喜欢音乐、喜欢折腾代码，偶尔写写生活感悟。欢迎来到我的小角落 🌿</p>
  </div>
</div>

<style>
  /* 包装层：占满首屏剩余高度，让云朵垂直+水平居中 */
  .about-wrap {
    display: flex; align-items: center; justify-content: center;
    min-height: calc(100vh - 320px);
  }

  .about-cloud {
    position: relative; width: min(88%, 540px);
    text-align: center; color: #42656F; font-size: 14px; line-height: 2;
  }
  .about-cloud p {
    position: relative; z-index: 1;
    margin: 0; padding: 24px 30px; background: #EAF4F5;
    border-radius: 38px; box-shadow: 0 4px 16px rgba(120, 150, 180, 0.2);
  }
  .about-cloud .p { position: absolute; background: #EAF4F5; border-radius: 50%; }
  .p1 { width: 64px; height: 64px; left: 7%; top: -24px; }
  .p2 { width: 46px; height: 46px; left: 30%; top: -30px; }
  .p3 { width: 38px; height: 38px; right: 24%; top: -16px; }
  .p4 { width: 30px; height: 30px; left: -14px; top: 40%; }
  .p5 { width: 28px; height: 28px; right: -10px; top: 36%; }
</style>

<script>
  document.querySelector(".dynamic-title") && document.querySelector(".dynamic-title").remove();
</script>