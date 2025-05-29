---
layout: default
title: 首页
---

<div class="header-section" style="background: linear-gradient(120deg, #E8F5E9, #F3E5F5); padding: 40px 0; text-align: center; border-radius: 10px; margin-bottom: 30px;">
  <h1 style="color: #2E7D32; margin-bottom: 20px;">小组会安排</h1>
  <p style="color: #4A4A4A; font-size: 1.2em;">本页面记录了我们研讨班的小组会安排和论文讨论记录</p>
</div>

每周四上午8:30-11:30，地点：计算机科学与技术学院会议室

> 🔔 新成员请查看[论文分享上传指南]({{ site.baseurl }}/docs/upload-guide)了解如何上传你的分享

<div class="meeting-rules" style="background: #F5F5F5; padding: 25px; border-radius: 10px; margin: 30px 0;">
  <h2 style="color: #1B5E20; border-bottom: 2px solid #81C784; padding-bottom: 10px; margin-bottom: 20px;">小组会制度：</h2>
  <ol>
    <li><strong>报告安排：</strong> 每周安排4位同学进行论文分享和研究进展汇报</li>
    <li><strong>论文选择：</strong> 优先选择近期发表于顶级会议/期刊的论文，与小组研究方向相关</li>
    <li><strong>报告准备：</strong>
      <ul>
        <li>精读论文，理解核心思想和创新点</li>
        <li>准备25-30分钟的演讲幻灯片</li>
        <li>可以适当补充相关工作的背景知识</li>
        <li>建议对论文方法进行复现或尝试改进</li>
      </ul>
    </li>
    <li><strong>讨论环节：</strong> 报告后留出15-20分钟的讨论时间，鼓励大家积极参与讨论</li>
    <li><strong>资料分享：</strong> 报告后请将论文、幻灯片和笔记上传至本网站，方便大家查阅</li>
  </ol>
</div>

{% include todo_list.md %}

## 论文分享列表

<style>
  .paper-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
    padding: 20px 0;
  }
  
  .paper-item {
    background: white;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .paper-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
  }
  
  .paper-item a {
    text-decoration: none;
    color: inherit;
  }
  
  .paper-item h3 {
    color: #1B5E20;
    margin-bottom: 10px;
  }
  
  .paper-item p {
    color: #666;
    margin: 5px 0;
  }
</style>

<div class="paper-list" id="paper-list">
  {% for post in site.posts %}
  <div class="paper-item">
    <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">
      <h3>{{ post.title }}</h3>
      <p>{{ post.journal }}</p>
      <p>报告人：{{ post.presenter }}</p>
      <p>日期：{{ post.date | date: "%Y-%m-%d" }}</p>
    </a>
  </div>
  {% endfor %}
</div>
