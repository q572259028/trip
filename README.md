<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width,initial-scale=1.0">
  <title>五天旅行时间表</title>
  <link href="https://fonts.googleapis.com/css?family=ZCOOL+XiaoWei|Roboto:400,700&display=swap" rel="stylesheet">
  <style>
    :root {
      --main-color: #3da9fc;
      --accent-color: #eab308;
      --bg-color: #f4f8fb;
      --section-bg: #fff;
      --border-radius: 16px;
      --shadow: 0 4px 16px 0 rgba(61,169,252,0.10);
      --font-main: 'ZCOOL XiaoWei', 'Roboto', Arial, sans-serif;
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      background: var(--bg-color);
      font-family: var(--font-main);
      color: #222;
      line-height: 1.7;
    }
    header {
      background: linear-gradient(90deg, var(--main-color), #56cfe1);
      color: white;
      padding: 2rem 1rem 1rem;
      text-align: center;
      border-bottom-left-radius: var(--border-radius);
      border-bottom-right-radius: var(--border-radius);
      box-shadow: var(--shadow);
    }
    header h1 {
      margin: 0;
      font-size: 2.2rem;
      letter-spacing: 2px;
      font-weight: 700;
    }
    header p {
      margin-top: .5rem;
      font-size: 1.1rem;
      letter-spacing: 1px;
    }
    main {
      max-width: 750px;
      margin: 2rem auto;
      padding: 0 1rem;
    }
    details {
      background: var(--section-bg);
      border-radius: var(--border-radius);
      margin-bottom: 1.5rem;
      box-shadow: var(--shadow);
      transition: box-shadow 0.3s;
      overflow: hidden;
    }
    details[open] {
      box-shadow: 0 8px 24px 0 rgba(61,169,252,0.18);
    }
    summary {
      cursor: pointer;
      padding: 1.2rem 1.5rem;
      font-size: 1.25rem;
      font-weight: 700;
      background: linear-gradient(90deg, var(--main-color) 80%, var(--accent-color) 100%);
      color: white;
      border-bottom: 1px solid #eaf3fa;
      border-radius: var(--border-radius) var(--border-radius) 0 0;
      outline: none;
      transition: background 0.2s;
    }
    details[open] summary {
      background: linear-gradient(90deg, var(--main-color) 60%, var(--accent-color) 100%);
    }
    .day-content {
      padding: 1.5rem 1.5rem 1rem 1.5rem;
      background: var(--section-bg);
    }
    .schedule-list {
      list-style: none;
      margin: 0 0 1rem 0;
      padding: 0;
    }
    .schedule-list li {
      margin-bottom: .7em;
      padding-left: 1.5em;
      position: relative;
      font-size: 1.08rem;
    }
    .schedule-list li::before {
      content: "⏰";
      position: absolute;
      left: 0;
      top: 0;
      color: var(--main-color);
      font-size: 1rem;
    }
    .section-title {
      font-size: 1.1rem;
      margin: 1.2em 0 .5em;
      color: var(--main-color);
      font-weight: 700;
      letter-spacing: 1px;
    }
    .tips, .strategy {
      background: #f7faff;
      border-left: 4px solid var(--main-color);
      padding: .8em 1em;
      margin-bottom: .7em;
      border-radius: 8px;
      font-size: .99rem;
    }
    .tips {
      background: #fefae0;
      border-left-color: var(--accent-color);
      color: #866311;
    }
    @media (max-width: 600px) {
      main {
        padding: 0 .3rem;
      }
      header {
        padding: 1.1rem .5rem .8rem;
      }
      .day-content {
        padding: 1rem;
      }
      summary {
        font-size: 1.07rem;
        padding: .85rem 1rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>五日旅行时间表</h1>
    <p>细致日程 · 景点攻略 · 温馨提示</p>
  </header>
  <main>
    <!-- 第一天 -->
    <details open>
      <summary>Day 1 · 4月29日<br>抵达与告庄夜市之夜</summary>
      <div class="day-content">
        <ul class="schedule-list">
          <li>21:30 抵达机场</li>
          <li>21:30-22:00 打车前往酒店</li>
          <li>22:00 入住酒店</li>
          <li>22:10 前往告庄夜市</li>
        </ul>
        <div class="section-title">景区攻略 · 告庄夜市</div>
        <div class="strategy">
          <ul>
            <li>推荐品尝傣味小吃和水果冰饮，夜市内有丰富的手工艺品和民族表演。</li>
            <li>夜市热闹但不拥挤，适合慢慢逛吃，注意保管好随身物品。</li>
          </ul>
        </div>
        <div class="section-title">注意事项</div>
        <div class="tips">
          <ul>
            <li>夜间出行注意安全，建议结伴而行。</li>
            <li>可提前在酒店办理入住，节省时间。</li>
          </ul>
        </div>
      </div>
    </details>
    <!-- 第二天 -->
    <details>
      <summary>Day 2 · 4月30日<br>植物园 & 傣族园深度游</summary>
      <div class="day-content">
        <ul class="schedule-list">
          <li>09:00 城市旅游集散地集合</li>
          <li>09:00-10:30 大巴前往植物园</li>
          <li>10:30-14:30 热带植物园（建议游览主要园区、观赏热带奇花异草）</li>
          <li>14:30-15:00 大巴前往傣族园</li>
          <li>15:00-17:30 傣族园（体验泼水节文化，欣赏傣族歌舞）</li>
          <li>17:30-19:00 大巴返回告庄</li>
          <li>19:30 椿梅私厨晚餐</li>
        </ul>
        <div class="section-title">景区攻略</div>
        <div class="strategy">
          <b>热带植物园：</b>
          <ul>
            <li>建议上午游览核心园区，拍照留念。</li>
            <li>园内有电瓶车可选择，炎热时注意防晒补水。</li>
          </ul>
          <b>傣族园：</b>
          <ul>
            <li>可体验泼水互动，建议带一套干净衣物换洗。</li>
            <li>感受傣族手工艺与美食，记得参与民俗表演。</li>
          </ul>
        </div>
        <div class="section-title">注意事项</div>
        <div class="tips">
          <ul>
            <li>户外活动较多，注意防晒，携带雨具。</li>
            <li>景区内步行较多，建议穿舒适鞋子。</li>
          </ul>
        </div>
      </div>
    </details>
    <!-- 第三天 -->
    <details>
      <summary>Day 3 · 5月1日<br>美食探店 & 曼听御花园</summary>
      <div class="day-content">
        <ul class="schedule-list">
          <li>10:00 云味坊早餐</li>
          <li>12:00 菌公主午餐（特色菌菇火锅）</li>
          <li>13:00 曼听御花园 & 总佛寺（文化体验与拍照圣地）</li>
          <li>16:00 春武里排队/烤肉糯米饭/水果交易中心</li>
          <li>19:00 春武里晚餐</li>
          <li>20:30 江边夜市（观夜景、品小吃）</li>
          <li>22:30 小玉烧烤/星光夜市</li>
        </ul>
        <div class="section-title">美食&景点攻略</div>
        <div class="strategy">
          <ul>
            <li><b>云味坊</b>：尝试本地米线、烧饵块。</li>
            <li><b>曼听御花园</b>：建议提前预约门票，欣赏傣族风情园林，留意佛寺礼仪。</li>
            <li><b>春武里</b>：傣味烤肉必试，建议错峰排队。</li>
            <li><b>夜市</b>：适合夜拍与休闲，品尝本地小吃。</li>
          </ul>
        </div>
        <div class="section-title">注意事项</div>
        <div class="tips">
          <ul>
            <li>部分餐厅/景区需排队，合理安排时间。</li>
            <li>尊重当地宗教习俗，佛寺内请勿喧哗。</li>
            <li>夜市人流量大，注意随身物品。</li>
          </ul>
        </div>
      </div>
    </details>
    <!-- 第四天 -->
    <details>
      <summary>Day 4 · 5月2日<br>抚仙湖日落 & 网红栈道</summary>
      <div class="day-content">
        <ul class="schedule-list">
          <li>07:30 高铁出发</li>
          <li>11:00 昆明南站</li>
          <li>11:45 机场大巴/汽车</li>
          <li>12:45 抵达抚仙湖希尔顿酒店，入住休整</li>
          <li>13:30 抗浪鱼午餐</li>
          <li>14:30 化石博物馆参观</li>
          <li>16:00 S湾、网红栈道观景（推荐拍照/看夕阳）</li>
          <li>19:00 星光夜市（湖畔夜景、特色小吃）</li>
        </ul>
        <div class="section-title">景区攻略</div>
        <div class="strategy">
          <ul>
            <li><b>抚仙湖</b>：水质清澈，适合拍照和骑行，注意环保。</li>
            <li><b>网红栈道</b>：日落时分光影极美，建议提前到达占位。</li>
            <li><b>化石博物馆</b>：适合亲子、涨知识，馆内可购纪念品。</li>
          </ul>
        </div>
        <div class="section-title">注意事项</div>
        <div class="tips">
          <ul>
            <li>湖边风大，建议带薄外套。</li>
            <li>拍照时注意安全，勿靠近深水区。</li>
            <li>酒店入住可提前联系前台确认。</li>
          </ul>
        </div>
      </div>
    </details>
    <!-- 第五天 -->
    <details>
      <summary>Day 5 · 5月3日<br>明星鱼洞 & 禄冲红沙滩</summary>
      <div class="day-content">
        <ul class="schedule-list">
          <li>10:00 出发（建议酒店早餐后出发）</li>
          <li>12:00 明星鱼洞附近午餐</li>
          <li>13:00 明星鱼洞帆船体验（湖面风光）</li>
          <li>15:00 禄冲古镇参观</li>
          <li>16:00 红沙滩漫步（适合拍照、观湖景）</li>
          <li>17:00 返回用餐/休息</li>
          <li>19:00 前往长水机场</li>
          <li>23:20 航班起飞</li>
        </ul>
        <div class="section-title">景区攻略</div>
        <div class="strategy">
          <ul>
            <li><b>明星鱼洞</b>：可体验帆船，建议穿防晒衣。</li>
            <li><b>禄冲古镇</b>：可购买特色小吃和手工艺品。</li>
            <li><b>红沙滩</b>：拍摄湖景与沙滩合影的好地方。</li>
          </ul>
        </div>
        <div class="section-title">注意事项</div>
        <div class="tips">
          <ul>
            <li>当天为返程日，合理安排行李整理和交通时间。</li>
            <li>建议预留充足时间前往机场，避免误机。</li>
            <li>景区户外活动多，防晒措施要到位。</li>
          </ul>
        </div>
      </div>
    </details>
    <!-- 结尾 -->
    <section style="text-align:center;color:#6b7280;margin:2.5em 0 1em;">
      <hr style="border:none;border-top:1px solid #eaeaea;margin:1em 0 1.5em;">
      <div>预祝旅途愉快！<br> by stshentu 。</div>
    </section>
  </main>
  <script>
    // 自动关闭其他天，只允许一个折叠项打开
    document.querySelectorAll("details").forEach((targetDetail) => {
      targetDetail.addEventListener("toggle", () => {
        if (targetDetail.open) {
          document.querySelectorAll("details").forEach((detail) => {
            if (detail !== targetDetail) {
              detail.open = false;
            }
          });
        }
      });
    });
  </script>
</body>
</html>
