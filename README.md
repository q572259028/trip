<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>西双版纳-抚仙湖行程表</title>
    <link href="https://cdn.bootcdn.net/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --primary-color: #2d5f2a;
            --secondary-color: #f0e6d4;
            --accent-color: #d4af37;
        }

        body {
            font-family: 'Segoe UI', system-ui;
            background: linear-gradient(135deg, #f5f5f5 0%, #e8f5e9 100%);
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .timeline-container {
            background: white;
            border-radius: 1rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            padding: 2rem;
            position: relative;
            overflow: hidden;
        }

        .day-card {
            border-left: 4px solid var(--primary-color);
            margin: 2rem 0;
            padding-left: 1.5rem;
            position: relative;
            transition: transform 0.3s ease;
        }

        .day-card:hover {
            transform: translateX(10px);
        }

        .timeline-badge {
            position: absolute;
            left: -2.2rem;
            top: -0.5rem;
            background: var(--primary-color);
            color: white;
            width: 3rem;
            height: 3rem;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        details {
            margin: 1rem 0;
            border: 1px solid #ddd;
            border-radius: 8px;
            transition: box-shadow 0.3s;
        }

        details:hover {
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        summary {
            padding: 1rem;
            background: var(--secondary-color);
            cursor: pointer;
            font-weight: 600;
            color: var(--primary-color);
            list-style: none;
            border-radius: 8px 8px 0 0;
        }

        summary::-webkit-details-marker {
            display: none;
        }

        .time-block {
            display: grid;
            grid-template-columns: 100px 1fr;
            gap: 1rem;
            padding: 1rem;
            border-bottom: 1px solid #eee;
        }

        .transportation {
            color: var(--accent-color);
            font-weight: 500;
            margin: 0.5rem 0;
        }

        .tips-card {
            background: #fff9e6;
            padding: 1rem;
            border-radius: 6px;
            margin: 1rem 0;
            border-left: 3px solid var(--accent-color);
        }

        @media print {
            body {
                padding: 0;
                background: white;
            }
            details {
                display: block;
            }
            summary {
                background: none;
            }
        }
    </style>
</head>
<body>
    <div class="timeline-container">
        <!-- 4月29日行程 -->
        <div class="day-card">
            <div class="timeline-badge">D1</div>
            <h2>4月29日 到达日</h2>
            <details open>
                <summary>行程详情 <i class="fas fa-chevron-down"></i></summary>
                <div class="time-block">
                    <div>21:30</div>
                    <div>
                        <strong>机场落地</strong>
                        <p class="transportation">预计22:00到达酒店</p>
                        <div class="tips-card">
                            <h4>告庄夜市攻略：</h4>
                            <ul>
                                <li>最佳拍照点：大金塔前广场</li>
                                <li>必尝小吃：傣味烧烤、舂鸡脚、椰子冰沙</li>
                                <li>购物提示：傣锦和手工银饰可适当砍价</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </details>
        </div>

        <!-- 4月30日行程 -->
        <div class="day-card">
            <div class="timeline-badge">D2</div>
            <h2>4月30日 经典景点日</h2>
            <details open>
                <summary>行程详情 <i class="fas fa-chevron-down"></i></summary>
                <!-- 植物园时段 -->
                <div class="time-block">
                    <div>09:00-14:30</div>
                    <div>
                        <strong>中科院植物园</strong>
                        <p class="transportation">大巴车程1.5小时</p>
                        <div class="tips-card">
                            <h4>游览建议：</h4>
                            <ul>
                                <li>西区适合拍照，东区适合徒步</li>
                                <li>必看景点：王莲池、奇花异卉园</li>
                                <li>准备防晒用具和驱蚊液</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- 傣族园时段 -->
                <div class="time-block">
                    <div>15:00-17:30</div>
                    <div>
                        <strong>傣族园</strong>
                        <p class="transportation">大巴车程0.5小时</p>
                        <div class="tips-card">
                            <h4>体验亮点：</h4>
                            <ul>
                                <li>每天14:50/16:50的泼水节活动</li>
                                <li>推荐参观曼春满古佛寺</li>
                                <li>可租借傣族服饰拍照</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </details>
        </div>

        <!-- 其他天数结构类似，此处省略详细代码 -->

        <!-- 注意事项板块 -->
        <details>
            <summary>重要注意事项 <i class="fas fa-exclamation-triangle"></i></summary>
            <div class="tips-card">
                <h3>旅行必备：</h3>
                <ul>
                    <li>高原防晒三件套：墨镜、帽子、SPF50+防晒霜</li>
                    <li>建议携带肠胃药和防蚊用品</li>
                    <li>各景区需要准备健康码和身份证</li>
                    <li>昼夜温差大，备薄外套</li>
                </ul>
            </div>
        </details>
    </div>

    <script>
        // 自动展开当天行程
        const today = new Date().getDate();
        document.querySelectorAll('.day-card').forEach(card => {
            const dayNumber = parseInt(card.querySelector('.timeline-badge').textContent.replace('D',''))
            if(dayNumber === Math.floor((today - 29 + 7)%7 + 1)) {
                card.querySelector('details').open = true;
            }
        });

        // 打印优化
        window.addEventListener('beforeprint', () => {
            document.querySelectorAll('details').forEach(d => d.open = true);
        });
    </script>
</body>
</html>
