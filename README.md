<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>西双版纳-抚仙湖五日深度游行程计划</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e67e22;
        }

        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background: #f8f9fa;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .timeline {
            position: relative;
            padding: 20px 0;
        }

        .day-card {
            background: white;
            border-radius: 12px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            overflow: hidden;
        }

        .day-header {
            background: var(--primary-color);
            color: white;
            padding: 15px 20px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .day-content {
            padding: 20px;
            display: none;
        }

        .time-item {
            display: flex;
            margin-bottom: 15px;
            position: relative;
            padding-left: 30px;
        }

        .time-item::before {
            content: "";
            position: absolute;
            left: 0;
            top: 5px;
            width: 12px;
            height: 12px;
            background: var(--secondary-color);
            border-radius: 50%;
        }

        .time {
            flex: 0 0 80px;
            color: var(--accent-color);
            font-weight: 500;
        }

        .tabs {
            display: flex;
            gap: 10px;
            margin: 20px 0;
        }

        .tab {
            padding: 10px 20px;
            border-radius: 20px;
            background: #eee;
            cursor: pointer;
            transition: all 0.3s;
        }

        .tab.active {
            background: var(--secondary-color);
            color: white;
        }

        .tips {
            background: #e3f2fd;
            padding: 15px;
            border-radius: 8px;
            margin-top: 20px;
        }

        @media (max-width: 768px) {
            .time-item {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 style="text-align: center; color: var(--primary-color); margin-bottom: 30px;">🌴 云南深度游行程计划 🌊</h1>
        
        <div class="timeline">
            <!-- 每天的内容通过JavaScript生成 -->
        </div>
    </div>

    <script>
        const itinerary = [
            {
                date: "29号",
                title: "抵达西双版纳",
                schedule: [
                    { time: "21:30", event: "落地机场" },
                    { time: "22:00", event: "到达酒店（告庄附近）" },
                    { time: "22:30", event: "告庄夜市" }
                ],
                tips: [
                    "💡 夜市购物记得砍价（一般可砍30%-50%）",
                    "🚖 机场到市区约30元打车费，建议使用滴滴",
                    "📸 大金塔夜景最佳拍摄时间：20:00-22:00"
                ]
            },
            // 其他天的数据类似，此处省略...
        ];

        function createDayHTML(day) {
            return `
                <div class="day-card">
                    <div class="day-header">
                        <h3>第${day.index}天 · ${day.date} ${day.title}</h3>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="day-content">
                        <div class="tabs">
                            <div class="tab active" data-tab="schedule">行程安排</div>
                            <div class="tab" data-tab="tips">攻略提示</div>
                        </div>
                        <div id="schedule">
                            ${day.schedule.map(item => `
                                <div class="time-item">
                                    <div class="time">${item.time}</div>
                                    <div class="event">${item.event}</div>
                                </div>
                            `).join('')}
                        </div>
                        <div class="tips" id="tips" style="display:none;">
                            <ul>
                                ${day.tips.map(tip => `<li>${tip}</li>`).join('')}
                            </ul>
                        </div>
                    </div>
                </div>
            `;
        }

        // 初始化页面
        function init() {
            const timeline = document.querySelector('.timeline');
            itinerary.forEach((day, index) => {
                day.index = index + 1;
                timeline.innerHTML += createDayHTML(day);
            });

            // 添加交互功能
            document.querySelectorAll('.day-header').forEach(header => {
                header.addEventListener('click', () => {
                    const content = header.nextElementSibling;
                    content.style.display = content.style.display === 'none' ? 'block' : 'none';
                    header.querySelector('i').classList.toggle('fa-chevron-up');
                });
            });

            document.querySelectorAll('.tab').forEach(tab => {
                tab.addEventListener('click', () => {
                    tab.parentElement.querySelector('.active').classList.remove('active');
                    tab.classList.add('active');
                    const tabType = tab.dataset.tab;
                    tab.closest('.day-content').querySelectorAll('div[id]').forEach(div => {
                        div.style.display = div.id === tabType ? 'block' : 'none';
                    });
                });
            });
        }

        init();
    </script>
</body>
</html>
