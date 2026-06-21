---
title: 摄影
date: 2026-06-21
---

# 摄影

这里放我的摄影作品。

<div class="photo-wall">

<img src="/photos/photo1.jpg" alt="摄影作品1">
<img src="/photos/photo2.jpg" alt="摄影作品2">
<img src="/photos/photo3.jpg" alt="摄影作品3">

</div>

<style>
.photo-wall {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 18px;
  margin-top: 25px;
}

.photo-wall img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 12px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.photo-wall img:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.18);
}
</style>