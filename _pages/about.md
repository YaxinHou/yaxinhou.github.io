---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
  :root {
    --text: #222222;
    --muted: #666666;
    --subtle: #8a8a8a;
    --line: #e9e9e9;
    --card: #fbfbfb;
    --accent: #2f5fa7;
    --accent-soft: #eef3fb;
    --name: #5a3da5;
    --maxw: 980px;
  }

  html {
    scroll-behavior: smooth;
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Arial, sans-serif;
    color: var(--text);
    background: #ffffff;
    font-size: 15px;
    line-height: 1.72;
    letter-spacing: 0.01em;
  }

  .page__content,
  .page {
    max-width: var(--maxw);
  }

  p, span, li, div {
    font-size: 0.96rem;
  }

  a {
    color: var(--accent);
    text-decoration: none;
  }

  a:hover {
    text-decoration: underline;
  }

  h3 {
    font-size: 1.08rem;
    font-weight: 700;
    color: #111111;
    margin: 2.2rem 0 0.95rem;
    padding-bottom: 0.45rem;
    border-bottom: 1px solid var(--line);
    letter-spacing: 0;
  }

  hr {
    border: none;
    border-top: 1px solid var(--line);
    margin: 2rem 0;
  }

  .lead-block {
    padding: 0.1rem 0 0.2rem;
  }

  .profile-wrapper {
    display: grid;
    grid-template-columns: minmax(0, 1fr) 150px;
    gap: 1.5rem;
    align-items: start;
  }

  .profile-content {
    min-width: 0;
  }

  .profile-content p {
    margin: 0;
    text-align: justify;
  }

  .profile-logos {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.7rem;
    align-items: center;
    justify-items: center;
    padding-top: 0.15rem;
  }

  .profile-logos a:first-child {
    grid-column: 1 / -1;
  }

  .profile-logos img {
    max-width: 70px;
    max-height: 70px;
    width: auto;
    height: auto;
    object-fit: contain;
    display: block;
    opacity: 0.94;
  }

  .news-box {
    border: 1px solid var(--line);
    border-radius: 10px;
    background: #fcfcfc;
    padding: 0.8rem 1rem;
    max-height: 320px;
    overflow-y: auto;
  }

  .news-item {
    display: grid;
    grid-template-columns: 88px 1fr;
    gap: 0.8rem;
    padding: 0.55rem 0;
    border-bottom: 1px solid #f0f0f0;
    align-items: start;
  }

  .news-item:last-child {
    border-bottom: none;
  }

  .news-date {
    color: var(--subtle);
    font-size: 0.88rem;
    white-space: nowrap;
  }

  .news-text {
    font-size: 0.94rem;
  }

  .section-note {
    color: var(--muted);
    font-size: 0.93rem;
    margin: -0.15rem 0 1rem;
  }

  .pie-chart-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-top: 0.9rem;
  }

  .pie-card {
    border: 1px solid var(--line);
    border-radius: 10px;
    background: #ffffff;
    padding: 0.8rem;
  }

  .stats-chart {
    width: 100%;
    height: 320px;
  }

  .pub-group-title {
    margin: 1rem 0 0.65rem;
    font-size: 0.98rem;
    font-weight: 700;
    color: #111;
  }

  .publication-container {
    display: grid;
    grid-template-columns: 220px minmax(0, 1fr);
    gap: 1rem;
    padding: 0.9rem;
    margin: 0 0 1rem;
    border: 1px solid var(--line);
    border-radius: 10px;
    background: #fff;
    align-items: start;
  }

  .publication-container img {
    width: 100%;
    max-width: 220px;
    height: 132px;
    object-fit: cover;
    border-radius: 8px;
    display: block;
    box-shadow: none;
  }

  .pub-img-wrapper {
    position: relative;
    width: fit-content;
  }

  .paper-badge {
    position: absolute;
    top: 8px;
    left: 8px;
    background: rgba(17,17,17,0.78);
    color: #fff;
    font-size: 0.72rem;
    line-height: 1;
    padding: 0.28rem 0.42rem;
    border-radius: 5px;
    font-weight: 600;
    letter-spacing: 0.01em;
  }

  .pub-venue {
    color: var(--accent);
    font-weight: 700;
  }

  .pub-title {
    font-weight: 600;
    color: #161616;
  }

  .pub-authors {
    margin-top: 0.28rem;
    color: #444;
    font-size: 0.93rem;
  }

  .my-name {
    color: var(--name);
    font-weight: 700;
  }

  .split-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  .info-card {
    border: 1px solid var(--line);
    border-radius: 10px;
    background: #fff;
    padding: 0.95rem 1rem;
  }

  .info-card h4 {
    font-size: 0.96rem;
    margin: 0 0 0.55rem;
    color: #111;
  }

  .clean-list,
  .clean-list ul {
    margin: 0;
    padding-left: 1.1rem;
  }

  .clean-list li {
    margin: 0.28rem 0;
    color: #333;
  }

  .contact-box {
    border: 1px solid var(--line);
    border-radius: 10px;
    background: #fff;
    padding: 1rem;
  }

  .contact-text {
    margin-bottom: 0.9rem;
    color: #333;
  }

  .map-wrap {
    display: flex;
    justify-content: center;
  }

  .map-box {
    width: 100%;
    max-width: 300px;
    overflow: hidden;
    border-radius: 8px;
    border: 1px solid var(--line);
  }

  .greedy-nav button {
    display: none !important;
  }

  @media (max-width: 900px) {
    .publication-container {
      grid-template-columns: 1fr;
    }

    .publication-container img {
      max-width: 100%;
      height: auto;
      aspect-ratio: 16 / 9;
    }
  }

  @media (max-width: 768px) {
    body {
      font-size: 14px;
    }

    .profile-wrapper,
    .pie-chart-grid,
    .split-grid {
      grid-template-columns: 1fr;
    }

    .profile-logos {
      grid-template-columns: repeat(3, auto);
      justify-content: start;
    }

    .profile-logos a:first-child {
      grid-column: auto;
    }

    .news-item {
      grid-template-columns: 1fr;
      gap: 0.18rem;
    }

    .stats-chart {
      height: 290px;
    }
  }
</style>

### Profile

<div class="lead-block">
  <div class="profile-wrapper">
    <div class="profile-content">
      <p>
        I am currently a Ph.D. student at Southeast University, under the supervision of
        <a href="https://jyh-learning.github.io"><strong>Assoc. Prof. Yuheng Jia</strong></a>.
        I received my M.S. degree from Henan University in 2023, under the supervision of
        <a href="https://cs.henu.edu.cn/info/1273/5566.htm"><strong>Prof. Chongsheng Zhang</strong></a>.
        Before that, I obtained my B.S. degree in 2020 from Henan Institute of Engineering.
        My research interests lie in machine learning, with a focus on long-tailed learning and weakly supervised learning.
      </p>
    </div>

    <div class="profile-logos">
      <a href="https://www.seu.edu.cn" target="_blank">
        <img src="./images/SEU.svg" alt="Southeast University" title="Southeast University">
      </a>
      <a href="https://cse.seu.edu.cn" target="_blank">
        <img src="./images/CS.png" alt="School of Computer Science and Engineering" title="School of Computer Science and Engineering">
      </a>
      <a href="https://www.palmlab.cn" target="_blank">
        <img src="./images/PALM.png" alt="Pattern Learning and Mining Lab" title="Pattern Learning and Mining Lab">
      </a>
    </div>
  </div>
</div>

### News

<div class="news-box">
  <div class="news-item">
    <div class="news-date">2026.01</div>
    <div class="news-text">Our work <em>"Samples Are Not Equal: A Sample Selection Approach for Deep Clustering"</em> is accepted by ICLR 2026. <a href="https://iclr.cc/virtual/2026/poster/10009380">Paper</a> · <a href="https://github.com/notoaudrey/Samples-Are-Not-Equal">Code</a></div>
  </div>
  <div class="news-item">
    <div class="news-date">2025.11</div>
    <div class="news-text">Our work <em>"DiCaP: Distribution-Calibrated Pseudo-labeling for Semi-Supervised Multi-Label Learning"</em> is accepted by AAAI 2026. <a href="https://ojs.aaai.org/index.php/AAAI/article/view/39302">Paper</a> · <a href="https://github.com/hb-studying/DiCaP">Code</a></div>
  </div>
  <div class="news-item">
    <div class="news-date">2025.10</div>
    <div class="news-text">Awarded the National Scholarship for Ph.D. students.</div>
  </div>
  <div class="news-item">
    <div class="news-date">2025.09</div>
    <div class="news-text">Our work <em>"Keep It on a Leash: Controllable Pseudo-label Generation Towards Realistic Long-Tailed Semi-Supervised Learning"</em> is accepted by NeurIPS 2025. <a href="https://neurips.cc/virtual/2025/loc/san-diego/poster/116160">Paper</a> · <a href="https://github.com/YaxinHou/CPG">Code</a></div>
  </div>
  <div class="news-item">
    <div class="news-date">2025.05</div>
    <div class="news-text">Our work <em>"A Square Peg in a Square Hole: Meta-Expert for Long-Tailed Semi-Supervised Learning"</em> is accepted by ICML 2025. <a href="https://icml.cc/virtual/2025/poster/44441">Paper</a> · <a href="https://github.com/YaxinHou/Meta-Expert">Code</a></div>
  </div>
</div>

### Publication Statistics

<div class="section-note">
  A brief overview of my publications by venue, including accepted and published papers listed on this homepage.
</div>

<div class="pie-chart-grid">
  <div class="pie-card">
    <div id="conference-chart" class="stats-chart"></div>
  </div>
  <div class="pie-card">
    <div id="journal-chart" class="stats-chart"></div>
  </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/echarts@5/dist/echarts.min.js"></script>
<script>
  const conferenceChart = echarts.init(document.getElementById('conference-chart'), null, { renderer: 'svg' });
  const journalChart = echarts.init(document.getElementById('journal-chart'), null, { renderer: 'svg' });

  const conferenceData = [
    { value: 1, name: 'ICLR' },
    { value: 1, name: 'NeurIPS' },
    { value: 1, name: 'ICML' },
    { value: 2, name: 'AAAI' }
  ];

  const journalData = [
    { value: 1, name: 'Inf. Sci.' }
  ];

  const conferenceTotal = conferenceData.reduce((sum, item) => sum + item.value, 0);
  const journalTotal = journalData.reduce((sum, item) => sum + item.value, 0);

  function buildPieOption(titleText, total, data, colors) {
    const isMobile = window.innerWidth <= 768;
    const isSmall = window.innerWidth <= 480;

    return {
      tooltip: {
        trigger: 'item',
        formatter: '{b}: {c} ({d}%)',
        backgroundColor: 'rgba(255,255,255,0.98)',
        borderColor: '#e6e6e6',
        borderWidth: 1,
        textStyle: {
          color: '#222',
          fontFamily: 'Arial, sans-serif',
          fontSize: 12
        }
      },
      legend: {
        top: 8,
        left: 'center',
        icon: 'circle',
        itemWidth: 10,
        itemHeight: 10,
        textStyle: {
          color: '#555',
          fontSize: isSmall ? 10 : 11,
          fontFamily: 'Arial, sans-serif'
        }
      },
      graphic: [
        {
          type: 'text',
          left: 'center',
          top: isMobile ? '47%' : '49%',
          style: {
            text: titleText,
            textAlign: 'center',
            fill: '#7a7a7a',
            fontSize: isSmall ? 11 : 12,
            fontWeight: 500,
            fontFamily: 'Arial, sans-serif'
          }
        },
        {
          type: 'text',
          left: 'center',
          top: isMobile ? '54%' : '56%',
          style: {
            text: String(total),
            textAlign: 'center',
            fill: '#222',
            fontSize: isSmall ? 18 : 22,
            fontWeight: 700,
            fontFamily: 'Arial, sans-serif'
          }
        }
      ],
      series: [
        {
          type: 'pie',
          radius: isMobile ? ['44%', '62%'] : ['50%', '68%'],
          center: ['50%', '58%'],
          itemStyle: {
            borderColor: '#ffffff',
            borderWidth: 2
          },
          label: {
            show: true,
            formatter: isMobile ? '{b}\n{c}' : '{b}: {c}',
            color: '#555',
            fontSize: isSmall ? 9 : 11,
            fontFamily: 'Arial, sans-serif'
          },
          labelLine: {
            length: isSmall ? 5 : 7,
            length2: isSmall ? 4 : 6,
            lineStyle: {
              color: '#c7c7c7'
            }
          },
          emphasis: {
            scale: true,
            scaleSize: 3
          },
          color: colors,
          data: data
        }
      ]
    };
  }

  function renderCharts() {
    conferenceChart.setOption(buildPieOption('Conference', conferenceTotal, conferenceData, ['#5877a6', '#7993ba', '#9ab0cd', '#c4d0e0']), true);
    journalChart.setOption(buildPieOption('Journal', journalTotal, journalData, ['#7a8fa8']), true);
    conferenceChart.resize();
    journalChart.resize();
  }

  renderCharts();
  let resizeTimer = null;
  window.addEventListener('resize', function () {
    clearTimeout(resizeTimer);
    resizeTimer = setTimeout(renderCharts, 150);
  });
</script>

### Publications

<div class="section-note">
  Papers are listed below in descending order by year of submission before publication, or year of publication. For a full list, please refer to my <a href="https://scholar.google.com.hk/citations?hl=zh-CN&user=-0IuShsAAAAJ">Google Scholar</a> page.
</div>

<div class="pub-group-title">Conference Papers</div>

<div class="publication-container">
  <div class="pub-img-wrapper">
    <div class="paper-badge">CCF A</div>
    <img src="./images/CPG.png" alt="Publication Image">
  </div>
  <div>
    <div class="pub-venue">[NeurIPS 2025]</div>
    <div class="pub-title">Keep It on a Leash: Controllable Pseudo-label Generation Towards Realistic Long-Tailed Semi-Supervised Learning.</div>
    <div class="pub-authors"><span class="my-name">Yaxin Hou</span>, Bo Han, Yuheng Jia, Hui Liu, Junhui Hou.</div>
  </div>
</div>

<div class="publication-container">
  <div class="pub-img-wrapper">
    <div class="paper-badge">CCF A</div>
    <img src="./images/Meta-Expert.png" alt="Publication Image">
  </div>
  <div>
    <div class="pub-venue">[ICML 2025]</div>
    <div class="pub-title">A Square Peg in a Square Hole: Meta-Expert for Long-Tailed Semi-Supervised Learning.</div>
    <div class="pub-authors"><span class="my-name">Yaxin Hou</span>, Yuheng Jia.</div>
  </div>
</div>

<div class="publication-container">
  <div class="pub-img-wrapper">
    <div class="paper-badge">CCF A</div>
    <img src="./images/QAST.png" alt="Publication Image">
  </div>
  <div>
    <div class="pub-venue">[AAAI 2023]</div>
    <div class="pub-title">Quality-Aware Self-Training on Differentiable Synthesis of Rare Relational Data.</div>
    <div class="pub-authors">Chongsheng Zhang, <span class="my-name">Yaxin Hou</span>, Ke Chen, Shuang Cao, Gaojuan Fan, Ji Liu.</div>
  </div>
</div>

<div class="pub-group-title">Journal Papers</div>

<div class="publication-container">
  <div class="pub-img-wrapper">
    <div class="paper-badge">CCF B</div>
    <img src="./images/imFTP.png" alt="Publication Image">
  </div>
  <div>
    <div class="pub-venue">[Inf. Sci. 2024]</div>
    <div class="pub-title">imFTP: Deep imbalance learning via fuzzy transition and prototypical learning.</div>
    <div class="pub-authors"><span class="my-name">Yaxin Hou</span>, Weiping Ding, Chongsheng Zhang.</div>
  </div>
</div>

### Professional Services

<div class="split-grid">
  <div class="info-card">
    <h4>Conference Reviewer / Program Committee Member</h4>
    <ul class="clean-list">
      <li>The International Conference on Machine Learning (ICML), 2026.</li>
      <li>The European Conference on Computer Vision (ECCV), 2026.</li>
      <li>The IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2026.</li>
      <li>The Annual Conference on Neural Information Processing Systems (NeurIPS), 2025.</li>
      <li>The IEEE International Symposium on Machine Learning and Media Computing (MLMC), 2025–2026.</li>
    </ul>
  </div>

  <div class="info-card">
    <h4>Journal Reviewer</h4>
    <ul class="clean-list">
      <li>International Journal of Machine Learning and Cybernetics (IJMLC).</li>
      <li>Transactions on Machine Learning Research (TMLR).</li>
      <li>Pattern Recognition (PR).</li>
    </ul>
  </div>
</div>

### Honors and Awards

<div class="split-grid">
  <div class="info-card">
    <h4>Scholarships</h4>
    <ul class="clean-list">
      <li>National Scholarship (2025, The Chinese Ministry of Education).</li>
      <li>Master's Academic Scholarship (2020, The Henan Department of Education).</li>
      <li>National Encouragement Scholarship (2019, The Henan Department of Education).</li>
      <li>National Encouragement Scholarship (2017, The Henan Department of Education).</li>
    </ul>
  </div>

  <div class="info-card">
    <h4>Honors</h4>
    <ul class="clean-list">
      <li>Merit Graduate Student (2025, Southeast University).</li>
      <li>Outstanding Graduate Student (2023, Henan University).</li>
      <li>Outstanding Graduate (2020, The Henan Department of Education).</li>
      <li>Merit Student (2020, The Henan Department of Education).</li>
    </ul>
  </div>
</div>

### Contact

<div class="contact-box">
  <div class="contact-text">
    Room 1009, Liberal Arts Building, School of Computer Science and Engineering.
  </div>

  <div class="map-wrap">
    <div class="map-box">
      <script type="text/javascript" id="mapmyvisitors" src="//mapmyvisitors.com/map.js?d=4D0h1VqEfuXzDioG4SfurpFAjXyS5BKdHFuIwYdKIHE&cl=ffffff&w=a"></script>
    </div>
  </div>
</div>
