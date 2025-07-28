<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <title>整形外科 | 新潟大学医学部 診療科ガイド</title>
  <link rel="stylesheet" href="../assets/style.css" />
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  <header>
    <h1>新潟大学医学部 診療科まとめ - 整形外科</h1>
    <nav><a href="../index.html">← トップに戻る</a></nav>
  </header>

  <main>
    <section>
      <h2>教授のビジョン・今後の予想</h2>
      <p>ロボット手術や再生医療などの先端医療技術を積極的に取り入れ、地域医療から国際的な貢献まで視野に入れている。</p>
    </section>

    <section>
      <h2>科の魅力</h2>
      <p>手技が多く、手術によって患者のQOLが劇的に改善するやりがいのある診療科。</p>
    </section>

    <section>
      <h2>ここは大変...</h2>
      <p>手術時間が長く、体力的にハードな一面もある。</p>
    </section>

    <section>
      <h2>教授の性格</h2>
      <p>論理的で研究熱心。若手にも積極的にチャンスを与えるタイプ。</p>
    </section>

    <section>
      <h2>医局の雰囲気</h2>
      <p>体育会系だが、風通しは良くオンオフの切り替えがしっかりしている。</p>
    </section>

    <section>
      <h2>患者の傾向</h2>
      <p>骨折や変形性関節症など高齢者の整形疾患が多いが、スポーツ整形も増加傾向。</p>
    </section>

    <section>
      <h2>求められる能力</h2>
      <p>体力、空間認識力、器用さ、粘り強さ。</p>
    </section>

    <section>
      <h2>取得可能な資格</h2>
      <ul>
        <li>整形外科専門医</li>
        <li>脊椎脊髄病認定医</li>
        <li>リハビリテーション認定医</li>
      </ul>
    </section>

    <section>
      <h2>科を選んだ理由（ランキング）</h2>
      <canvas id="reasonChart" width="400" height="200"></canvas>
    </section>

    <section>
      <h2>キャリアパスの選択肢</h2>
      <ul>
        <li>大学病院勤務（専門外来）</li>
        <li>市中病院整形外科医長</li>
        <li>開業（スポーツ整形・一般整形）</li>
        <li>海外フェローシップ</li>
      </ul>
    </section>

    <section>
      <h2>年収・忙しさグラフ</h2>
      <canvas id="careerChart" width="600" height="300"></canvas>
    </section>

    <section>
      <h2>大学院の種類</h2>
      <ul>
        <li>運動器バイオメカニクス研究</li>
        <li>骨再生医療研究</li>
      </ul>
    </section>

    <section>
      <h2>留学の種類</h2>
      <ul>
        <li>米国（関節外科）</li>
        <li>ドイツ（脊椎外科）</li>
      </ul>
    </section>

    <section>
      <h2>専攻医の深掘り</h2>

      <h3>5年目までの異動</h3>
      <p>初期研修→関連病院→大学病院→研究所→大学院</p>

      <h3>1日のスケジュール</h3>
      <canvas id="dailyChart" width="300" height="300"></canvas>

      <h3>業務内容</h3>
      <p>手術、術前術後管理、病棟回診、外来、カンファレンスなど。</p>

      <h3>年間スケジュール</h3>
      <p>4月：新年度配属／7月：手術手技講習会／10月：学会発表／12月：忘年会</p>
    </section>

    <section>
      <h2>先生インタビュー</h2>
      <a href="interview_orthopedics.html">→ 整形外科の先生インタビューを見る</a>
    </section>
  </main>

  <script>
    // 理由ランキング
    new Chart(document.getElementById('reasonChart'), {
      type: 'bar',
      data: {
        labels: ['手技中心', '治療効果が明確', 'スポーツに関われる'],
        datasets: [{
          label: '選択理由',
          data: [40, 35, 25],
          backgroundColor: ['#4e79a7', '#f28e2b', '#e15759']
        }]
      },
      options: {
        responsive: true,
        scales: {
          y: { beginAtZero: true }
        }
      }
    });

    // 年収・忙しさ推移
    new Chart(document.getElementById('careerChart'), {
      type: 'line',
      data: {
        labels: [...Array(15).keys()].map(i => `年${i + 1}`),
        datasets: [
          {
            label: '年収（万円）',
            data: [400, 450, 500, 550, 600, 700, 800, 900, 950, 1000, 1050, 1100, 1150, 1200, 1300],
            borderColor: '#4e79a7',
            yAxisID: 'y1'
          },
          {
            label: '忙しさ（10段階）',
            data: [6, 7, 8, 8, 7, 7, 6, 6, 5, 5, 5, 4, 4, 3, 3],
            borderColor: '#e15759',
            yAxisID: 'y2'
          }
        ]
      },
      options: {
        responsive: true,
        scales: {
          y1: {
            type: 'linear',
            position: 'left',
            title: { display: true, text: '年収（万円）' }
          },
          y2: {
            type: 'linear',
            position: 'right',
            title: { display: true, text: '忙しさ' },
            grid: { drawOnChartArea: false }
          }
        }
      }
    });

    // 1日のスケジュール
    new Chart(document.getElementById('dailyChart'), {
      type: 'pie',
      data: {
        labels: ['手術', '病棟業務', '外来', 'その他'],
        datasets: [{
          data: [5, 3, 2, 2],
          backgroundColor: ['#59a14f', '#edc949', '#af7aa1', '#76b7b2']
        }]
      }
    });
  </script>
</body>
</html>
