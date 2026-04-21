### 📊 Publication Statistics

<div class="stats-section">
  <div class="stats-header">
    <div>
      <div class="stats-kicker">Academic Snapshot</div>
      <div class="section-note stats-note">
        A brief overview of publications by venue, including accepted and published papers listed on this homepage.
      </div>
    </div>

    <div class="stats-summary">
      <div class="stats-summary-item">
        <span class="stats-summary-label">Total</span>
        <span class="stats-summary-value">6</span>
      </div>
      <div class="stats-summary-item">
        <span class="stats-summary-label">Conference</span>
        <span class="stats-summary-value">5</span>
      </div>
      <div class="stats-summary-item">
        <span class="stats-summary-label">Journal</span>
        <span class="stats-summary-value">1</span>
      </div>
    </div>
  </div>

  <div class="stats-wrap refined-stats-wrap">
    <div class="stats-card refined-stats-card">
      <div class="stats-card-head">
        <div class="stats-card-title">Conference Papers</div>
        <div class="stats-card-subtitle">By venue</div>
      </div>
      <div id="conference-chart" class="stats-chart"></div>
    </div>

    <div class="stats-card refined-stats-card">
      <div class="stats-card-head">
        <div class="stats-card-title">Journal Papers</div>
        <div class="stats-card-subtitle">By venue</div>
      </div>
      <div id="journal-chart" class="stats-chart"></div>
    </div>
  </div>

  <div class="stats-footer-note">
    Currently listed on this homepage:
    <strong>6 papers</strong>,
    including <strong>5 conference papers</strong> and
    <strong>1 journal paper</strong>.
  </div>
</div>

<style>
  .stats-section {
    margin-top: 0.2rem;
  }

  .stats-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    gap: 1rem;
    margin-bottom: 1rem;
    flex-wrap: wrap;
  }

  .stats-kicker {
    display: inline-flex;
    align-items: center;
    padding: 0.32rem 0.72rem;
    border-radius: 999px;
    background: linear-gradient(180deg, #f3f8fd 0%, #ebf3fa 100%);
    border: 1px solid #d8e5f1;
    color: var(--accent);
    font-size: 0.76rem;
    font-weight: 800;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    margin-bottom: 0.7rem;
    box-shadow: var(--shadow-xs);
  }

  .stats-note {
    margin: 0;
    max-width: 720px;
  }

  .stats-summary {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
  }

  .stats-summary-item {
    min-width: 92px;
    padding: 0.72rem 0.9rem;
    border-radius: 18px;
    background: linear-gradient(180deg, rgba(255,255,255,0.98) 0%, rgba(249,252,255,0.98) 100%);
    border: 1px solid var(--line);
    box-shadow: var(--shadow-xs);
    text-align: center;
  }

  .stats-summary-label {
    display: block;
    font-size: 0.74rem;
    font-weight: 700;
    color: var(--muted);
    letter-spacing: 0.02em;
    margin-bottom: 0.28rem;
  }

  .stats-summary-value {
    display: block;
    font-size: 1.35rem;
    line-height: 1;
    font-weight: 800;
    color: var(--title);
  }

  .refined-stats-wrap {
    gap: 1.1rem;
  }

  .refined-stats-card {
    position: relative;
    padding: 1.15rem 1rem 1rem;
    overflow: hidden;
  }

  .refined-stats-card::before {
    content: '';
    position: absolute;
    inset: 0 0 auto 0;
    height: 3px;
    background: linear-gradient(90deg, rgba(36, 91, 146, 0.95), rgba(143, 178, 209, 0.45), rgba(255,255,255,0));
  }

  .stats-card-head {
    text-align: center;
    margin-bottom: 0.35rem;
  }

  .stats-card-title {
    font-size: 0.98rem;
    font-weight: 800;
    color: var(--title);
    letter-spacing: 0.01em;
  }

  .stats-card-subtitle {
    margin-top: 0.18rem;
    font-size: 0.8rem;
    color: var(--muted);
  }

  .stats-footer-note {
    margin-top: 0.95rem;
    padding: 0.9rem 1rem;
    border: 1px solid var(--line);
    border-radius: 18px;
    background: linear-gradient(180deg, rgba(255,255,255,0.96) 0%, rgba(248,251,254,0.96) 100%);
    color: var(--muted);
    font-size: 0.92rem;
    line-height: 1.7;
    box-shadow: var(--shadow-xs);
  }

  @media (max-width: 640px) {
    .stats-summary {
      width: 100%;
    }

    .stats-summary-item {
      flex: 1 1 calc(33.333% - 0.5rem);
      min-width: 84px;
      padding: 0.65rem 0.7rem;
    }

    .stats-summary-value {
      font-size: 1.18rem;
    }

    .stats-footer-note {
      padding: 0.82rem 0.9rem;
    }
  }
</style>

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

  function buildPieOption(title, total, data, colors) {
    const isMobile = window.innerWidth <= 768;

    return {
      tooltip: {
        trigger: 'item',
        formatter: '{b}: {c} ({d}%)',
        backgroundColor: 'rgba(255,255,255,0.98)',
        borderColor: '#e7ebf0',
        borderWidth: 1,
        textStyle: {
          color: '#1f2328',
          fontFamily: 'Inter, Arial, sans-serif'
        }
      },
      color: colors,
      legend: {
        bottom: isMobile ? 0 : 4,
        left: 'center',
        icon: 'circle',
        itemWidth: 10,
        itemHeight: 10,
        itemGap: 16,
        textStyle: {
          color: '#4b5563',
          fontSize: isMobile ? 11 : 12,
          fontFamily: 'Inter, Arial, sans-serif'
        }
      },
      graphic: [
        {
          type: 'text',
          left: 'center',
          top: '42%',
          style: {
            text: title,
            textAlign: 'center',
            fill: '#6b7280',
            fontSize: isMobile ? 11 : 12,
            fontWeight: 600,
            fontFamily: 'Inter, Arial, sans-serif'
          }
        },
        {
          type: 'text',
          left: 'center',
          top: '50%',
          style: {
            text: String(total),
            textAlign: 'center',
            fill: '#0f172a',
            fontSize: isMobile ? 22 : 24,
            fontWeight: 800,
            fontFamily: 'Inter, Arial, sans-serif'
          }
        }
      ],
      series: [
        {
          type: 'pie',
          radius: isMobile ? ['42%', '60%'] : ['48%', '66%'],
          center: ['50%', '46%'],
          minAngle: 8,
          avoidLabelOverlap: true,
          itemStyle: {
            borderColor: '#ffffff',
            borderWidth: 3,
            shadowBlur: 10,
            shadowColor: 'rgba(15, 23, 42, 0.05)'
          },
          label: {
            color: '#475467',
            fontSize: isMobile ? 10 : 11,
            fontWeight: 600,
            formatter: isMobile ? '{b}\n{c}' : '{b}: {c}'
          },
          labelLine: {
            length: isMobile ? 8 : 10,
            length2: isMobile ? 8 : 12,
            lineStyle: {
              color: '#cbd5e1'
            }
          },
          emphasis: {
            scale: true,
            scaleSize: 4
          },
          data: data
        }
      ]
    };
  }

  function renderCharts() {
    conferenceChart.setOption(
      buildPieOption('Conference', 5, conferenceData, ['#2f5f8f', '#4f7aa6', '#7b9bbb', '#b7c8d9']),
      true
    );
    journalChart.setOption(
      buildPieOption('Journal', 1, journalData, ['#5b7ea3']),
      true
    );
    conferenceChart.resize();
    journalChart.resize();
  }

  renderCharts();

  if (typeof ResizeObserver !== 'undefined') {
    const chartContainers = [
      document.getElementById('conference-chart'),
      document.getElementById('journal-chart')
    ].filter(Boolean);

    const resizeObserver = new ResizeObserver(function () {
      conferenceChart.resize();
      journalChart.resize();
    });

    chartContainers.forEach(function (el) {
      resizeObserver.observe(el);
    });
  } else {
    let resizeTimer = null;
    window.addEventListener('resize', function () {
      clearTimeout(resizeTimer);
      resizeTimer = setTimeout(function () {
        conferenceChart.resize();
        journalChart.resize();
      }, 120);
    });
  }
</script>
