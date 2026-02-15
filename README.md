<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>令和8年 釣部釣友会 春合宿しおり</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Yu Gothic', 'Hiragino Kaku Gothic ProN', 'Meiryo', sans-serif;
            line-height: 1.7;
            color: #2c3e50;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 0;
        }
        
        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: #ffffff;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
        
        .header {
            background: linear-gradient(135deg, #2c5aa0 0%, #1e3c72 100%);
            color: #ffffff;
            padding: 40px 30px 30px;
            text-align: center;
            position: relative;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }
        
        .header::before {
            content: '🎣';
            position: absolute;
            top: 15px;
            left: 20px;
            font-size: 2em;
            opacity: 0.3;
        }
        
        .header::after {
            content: '♨️';
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 2em;
            opacity: 0.3;
        }
        
        .header h1 {
            font-size: 1.8em;
            margin-bottom: 12px;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
            font-weight: 700;
        }
        
        .header .subtitle {
            font-size: 1.3em;
            margin-bottom: 10px;
            color: #ffd700;
            font-weight: 600;
            letter-spacing: 1px;
        }
        
        .header .tagline {
            font-size: 1.1em;
            color: #a8dadc;
            font-style: italic;
            margin-top: 8px;
        }
        
        /* タブナビゲーション */
        .tab-nav {
            background: #ffffff;
            display: flex;
            overflow-x: auto;
            border-bottom: 3px solid #e9ecef;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            -webkit-overflow-scrolling: touch;
        }
        
        .tab-nav::-webkit-scrollbar {
            height: 4px;
        }
        
        .tab-nav::-webkit-scrollbar-thumb {
            background: #2c5aa0;
            border-radius: 2px;
        }
        
        .tab-button {
            flex: 1;
            min-width: 120px;
            padding: 18px 15px;
            background: #f8f9fa;
            border: none;
            cursor: pointer;
            font-size: 1em;
            font-weight: 600;
            color: #546e7a;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            white-space: nowrap;
        }
        
        .tab-button:hover {
            background: #e3f2fd;
            color: #2c5aa0;
        }
        
        .tab-button.active {
            background: #ffffff;
            color: #1e3c72;
            border-bottom-color: #2c5aa0;
            font-weight: 700;
        }
        
        .tab-icon {
            font-size: 1.3em;
        }
        
        /* タブコンテンツ */
        .tab-content {
            display: none;
            padding: 30px 25px 50px;
            background: #f8f9fa;
            flex: 1;
            animation: fadeIn 0.4s ease;
        }
        
        .tab-content.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .section {
            margin-bottom: 30px;
            padding: 30px;
            background: #ffffff;
            border-radius: 12px;
            border-left: 6px solid #2c5aa0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.08);
        }
        
        .section-title {
            font-size: 1.75em;
            color: #1e3c72;
            margin-bottom: 25px;
            padding-bottom: 12px;
            border-bottom: 3px solid #2c5aa0;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .info-grid {
            display: grid;
            gap: 15px;
        }
        
        .info-item {
            display: flex;
            padding: 16px 20px;
            background: #f8f9fa;
            border-radius: 10px;
            border: 1px solid #e9ecef;
            transition: all 0.3s ease;
        }
        
        .info-item:hover {
            background: #e3f2fd;
            border-color: #2c5aa0;
            transform: translateX(5px);
        }
        
        .info-label {
            font-weight: 700;
            color: #2c5aa0;
            min-width: 140px;
            font-size: 1.05em;
        }
        
        .info-value {
            flex: 1;
            color: #34495e;
            font-size: 1.05em;
        }
        
        .emergency {
            background: linear-gradient(135deg, #fff3cd 0%, #ffe6a7 100%);
            border: 2px solid #ff6b6b;
            border-left-width: 6px;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }
        
        .emergency .info-item {
            background: rgba(255,255,255,0.7);
        }
        
        .emergency .info-label {
            color: #d32f2f;
            font-size: 1.1em;
        }
        
        .emergency .info-value {
            color: #d32f2f;
            font-weight: 600;
            font-size: 1.15em;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            background: #ffffff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            font-size: 1.05em;
        }
        
        th {
            background: linear-gradient(135deg, #2c5aa0 0%, #1e3c72 100%);
            color: #ffffff;
            padding: 16px 15px;
            text-align: left;
            font-weight: 700;
            font-size: 1.05em;
        }
        
        td {
            padding: 14px 15px;
            border-bottom: 1px solid #e9ecef;
            color: #2c3e50;
        }
        
        tr:hover {
            background: #f1f8ff;
        }
        
        .day-header {
            background: linear-gradient(135deg, #e3f2fd 0%, #bbdefb 100%);
            font-weight: 700;
            color: #1565c0;
            font-size: 1.1em;
        }
        
        .day-header td {
            padding: 16px 15px;
        }
        
        .checklist {
            list-style: none;
            padding: 0;
            display: grid;
            gap: 12px;
        }
        
        .checklist li {
            padding: 16px 20px;
            background: #f8f9fa;
            border-radius: 10px;
            border: 2px solid #e9ecef;
            display: flex;
            align-items: center;
            transition: all 0.3s ease;
            font-size: 1.05em;
            color: #2c3e50;
            cursor: pointer;
            user-select: none;
        }
        
        .checklist li:hover {
            background: #e8f5e9;
            border-color: #4caf50;
            transform: translateX(5px);
        }
        
        .checklist li.checked {
            background: #c8e6c9;
            border-color: #4caf50;
            text-decoration: line-through;
            opacity: 0.7;
        }
        
        .checklist li::before {
            content: "☐";
            font-size: 1.8em;
            margin-right: 18px;
            color: #2c5aa0;
            font-weight: bold;
        }
        
        .checklist li.checked::before {
            content: "☑";
            color: #4caf50;
        }
        
        .room-group {
            margin-bottom: 20px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 10px;
            border: 2px solid #e9ecef;
            transition: all 0.3s ease;
        }
        
        .room-group:hover {
            background: #e3f2fd;
            border-color: #2c5aa0;
        }
        
        .room-title {
            font-weight: 700;
            color: #1e3c72;
            margin-bottom: 12px;
            font-size: 1.2em;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .member-list {
            padding-left: 25px;
            color: #34495e;
            line-height: 1.8;
            font-size: 1.05em;
        }
        
        .warning-box {
            background: linear-gradient(135deg, #fff9e6 0%, #ffecb3 100%);
            border: 3px solid #ffa726;
            border-radius: 12px;
            padding: 25px;
            margin-top: 20px;
        }
        
        .warning-title {
            color: #e65100;
            font-weight: 700;
            font-size: 1.3em;
            margin-bottom: 18px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .warning-title::before {
            content: '⚠️';
            font-size: 1.3em;
        }
        
        .warning-box ul {
            list-style-position: inside;
            color: #5d4037;
        }
        
        .warning-box li {
            margin-bottom: 14px;
            padding-left: 10px;
            line-height: 1.7;
            font-size: 1.05em;
        }
        
        .footer {
            background: #1e3c72;
            color: #ffffff;
            text-align: center;
            padding: 25px;
            margin-top: auto;
        }
        
        .footer p {
            font-size: 1em;
            opacity: 0.9;
        }
        
        /* 印刷用スタイル */
        @media print {
            body {
                background: white;
            }
            
            .container {
                box-shadow: none;
            }
            
            .tab-nav {
                display: none;
            }
            
            .tab-content {
                display: block !important;
                page-break-after: always;
            }
            
            .section {
                page-break-inside: avoid;
            }
        }
        
        /* レスポンシブ対応 */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 1.5em;
            }
            
            .header .subtitle {
                font-size: 1.1em;
            }
            
            .tab-button {
                min-width: 100px;
                padding: 15px 10px;
                font-size: 0.9em;
            }
            
            .tab-icon {
                font-size: 1.1em;
            }
            
            .section {
                padding: 20px;
            }
            
            .section-title {
                font-size: 1.4em;
            }
            
            .info-item {
                flex-direction: column;
                gap: 8px;
            }
            
            .info-label {
                min-width: auto;
            }
            
            table {
                font-size: 0.9em;
            }
            
            th, td {
                padding: 10px 8px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <h1>令和8年 釣部釣友会</h1>
            <div class="subtitle">春合宿しおり</div>
            <div class="tagline">大物を狙え!温泉と釣りの贅沢な3日間</div>
        </header>
        
        <nav class="tab-nav" role="tablist">
            <button class="tab-button active" onclick="switchTab(event, 'overview')" role="tab" aria-selected="true">
                <span class="tab-icon">📋</span>
                <span>概要</span>
            </button>
            <button class="tab-button" onclick="switchTab(event, 'schedule')" role="tab">
                <span class="tab-icon">📅</span>
                <span>スケジュール</span>
            </button>
            <button class="tab-button" onclick="switchTab(event, 'packing')" role="tab">
                <span class="tab-icon">🎒</span>
                <span>持ち物</span>
            </button>
            <button class="tab-button" onclick="switchTab(event, 'rooms')" role="tab">
                <span class="tab-icon">🏠</span>
                <span>部屋割り</span>
            </button>
            <button class="tab-button" onclick="switchTab(event, 'notes')" role="tab">
                <span class="tab-icon">⚠️</span>
                <span>注意事項</span>
            </button>
        </nav>
        
        <!-- 概要タブ -->
        <div id="overview" class="tab-content active">
            <section class="section">
                <h2 class="section-title">
                    <span>📍</span>
                    合宿基本情報
                </h2>
                <div class="info-grid">
                    <div class="info-item">
                        <span class="info-label">開催日程:</span>
                        <span class="info-value">2026年4月17日(金) 〜 4月19日(日) 2泊3日</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">宿泊施設:</span>
                        <span class="info-value">清流荘 温泉旅館</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">住所:</span>
                        <span class="info-value">〒123-4567 山梨県南都留郡富士河口湖町本栖128</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">電話:</span>
                        <span class="info-value">0555-87-1234</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">釣り場:</span>
                        <span class="info-value">本栖湖、精進湖周辺エリア</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">参加人数:</span>
                        <span class="info-value">16名</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">集合場所:</span>
                        <span class="info-value">新宿駅西口 バスターミナル</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">集合時間:</span>
                        <span class="info-value">4月17日(金) 7:00 AM (厳守)</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">解散予定:</span>
                        <span class="info-value">4月19日(日) 18:00 新宿駅</span>
                    </div>
                </div>
                
                <div class="emergency">
                    <h3 class="section-title" style="border: none; margin-bottom: 15px; font-size: 1.4em;">
                        <span>🚨</span>
                        緊急連絡先
                    </h3>
                    <div class="info-grid">
                        <div class="info-item">
                            <span class="info-label">幹事(田中):</span>
                            <span class="info-value">090-1234-5678</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">副幹事(佐藤):</span>
                            <span class="info-value">080-9876-5432</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">宿泊施設:</span>
                            <span class="info-value">0555-87-1234</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">最寄り警察:</span>
                            <span class="info-value">富士吉田警察署 0555-22-0110</span>
                        </div>
                        <div class="info-item">
                            <span class="info-label">最寄り病院:</span>
                            <span class="info-value">富士吉田市立病院 0555-22-4111</span>
                        </div>
                    </div>
                </div>
            </section>
            
            <section class="section">
                <h2 class="section-title">
                    <span>💰</span>
                    費用について
                </h2>
                <div class="info-grid">
                    <div class="info-item">
                        <span class="info-label">参加費:</span>
                        <span class="info-value">¥28,000 / 人</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">含まれるもの:</span>
                        <span class="info-value">宿泊費(2泊)、食事(朝2回・夕2回)、バス代、釣り場利用料、保険料</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">含まれないもの:</span>
                        <span class="info-value">昼食代、個人的な飲食・買い物、エサ・仕掛け代</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">支払期限:</span>
                        <span class="info-value">4月10日(木) まで</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">支払方法:</span>
                        <span class="info-value">幹事 田中へ現金またはPayPay送金</span>
                    </div>
                </div>
            </section>
        </div>
        
        <!-- スケジュールタブ -->
        <div id="schedule" class="tab-content">
            <section class="section">
                <h2 class="section-title">
                    <span>📅</span>
                    3日間のスケジュール
                </h2>
                
                <table>
                    <thead>
                        <tr>
                            <th style="width: 120px;">時間</th>
                            <th>活動内容</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class="day-header">
                            <td colspan="2">🌅 1日目 - 4月17日(金)</td>
                        </tr>
                        <tr>
                            <td>07:00</td>
                            <td>新宿駅西口集合</td>
                        </tr>
                        <tr>
                            <td>07:30</td>
                            <td>貸切バス出発</td>
                        </tr>
                        <tr>
                            <td>09:30</td>
                            <td>途中休憩(談合坂SA)</td>
                        </tr>
                        <tr>
                            <td>11:00</td>
                            <td>宿到着・チェックイン</td>
                        </tr>
                        <tr>
                            <td>11:30</td>
                            <td>昼食(各自・周辺食堂)</td>
                        </tr>
                        <tr>
                            <td>13:00</td>
                            <td>本栖湖へ移動・午後の釣り開始</td>
                        </tr>
                        <tr>
                            <td>17:00</td>
                            <td>釣り終了・宿へ戻る</td>
                        </tr>
                        <tr>
                            <td>18:00</td>
                            <td>温泉入浴</td>
                        </tr>
                        <tr>
                            <td>19:00</td>
                            <td>夕食(会場食)</td>
                        </tr>
                        <tr>
                            <td>21:00</td>
                            <td>釣果発表会・懇親会</td>
                        </tr>
                        <tr>
                            <td>23:00</td>
                            <td>就寝</td>
                        </tr>
                        
                        <tr class="day-header">
                            <td colspan="2">☀️ 2日目 - 4月18日(土)</td>
                        </tr>
                        <tr>
                            <td>06:00</td>
                            <td>起床・朝風呂(任意)</td>
                        </tr>
                        <tr>
                            <td>07:00</td>
                            <td>朝食</td>
                        </tr>
                        <tr>
                            <td>08:00</td>
                            <td>精進湖へ移動・午前の釣り開始</td>
                        </tr>
                        <tr>
                            <td>12:00</td>
                            <td>昼食(各自・お弁当推奨)</td>
                        </tr>
                        <tr>
                            <td>13:00</td>
                            <td>午後の釣り再開</td>
                        </tr>
                        <tr>
                            <td>17:00</td>
                            <td>釣り終了・宿へ戻る</td>
                        </tr>
                        <tr>
                            <td>18:00</td>
                            <td>温泉入浴</td>
                        </tr>
                        <tr>
                            <td>19:00</td>
                            <td>夕食(BBQ)</td>
                        </tr>
                        <tr>
                            <td>21:00</td>
                            <td>大物釣果コンテスト表彰式・自由時間</td>
                        </tr>
                        <tr>
                            <td>23:00</td>
                            <td>就寝</td>
                        </tr>
                        
                        <tr class="day-header">
                            <td colspan="2">🏠 3日目 - 4月19日(日)</td>
                        </tr>
                        <tr>
                            <td>07:00</td>
                            <td>起床・朝風呂(任意)</td>
                        </tr>
                        <tr>
                            <td>08:00</td>
                            <td>朝食</td>
                        </tr>
                        <tr>
                            <td>09:00</td>
                            <td>本栖湖周辺で最終釣り</td>
                        </tr>
                        <tr>
                            <td>11:30</td>
                            <td>釣り終了・チェックアウト準備</td>
                        </tr>
                        <tr>
                            <td>12:00</td>
                            <td>昼食(各自・周辺食堂)</td>
                        </tr>
                        <tr>
                            <td>13:00</td>
                            <td>宿出発</td>
                        </tr>
                        <tr>
                            <td>15:00</td>
                            <td>途中休憩(石川PA)</td>
                        </tr>
                        <tr>
                            <td>18:00</td>
                            <td>新宿駅到着・解散</td>
                        </tr>
                    </tbody>
                </table>
            </section>
        </div>
        
        <!-- 持ち物タブ -->
        <div id="packing" class="tab-content">
            <section class="section">
                <h2 class="section-title">
                    <span>🎒</span>
                    持ち物チェックリスト
                </h2>
                
                <h3 style="color: #1e3c72; font-size: 1.3em; margin: 25px 0 15px; font-weight: 700;">必須アイテム</h3>
                <ul class="checklist">
                    <li>釣り竿・リール</li>
                    <li>仕掛け・ルアー・エサ</li>
                    <li>クーラーボックス</li>
                    <li>ライフジャケット(必須)</li>
                    <li>着替え(2〜3日分)</li>
                    <li>パジャマ・部屋着</li>
                    <li>タオル・バスタオル</li>
                    <li>洗面用具</li>
                    <li>常備薬</li>
                    <li>健康保険証のコピー</li>
                    <li>現金(3万円程度)</li>
                    <li>身分証明書</li>
                </ul>
                
                <h3 style="color: #1e3c72; font-size: 1.3em; margin: 35px 0 15px; font-weight: 700;">推奨アイテム</h3>
                <ul class="checklist">
                    <li>防水・防寒ウェア</li>
                    <li>レインコート</li>
                    <li>帽子・サングラス</li>
                    <li>日焼け止め</li>
                    <li>虫除けスプレー</li>
                    <li>ビニール袋(複数枚)</li>
                    <li>懐中電灯・ヘッドライト</li>
                    <li>モバイルバッテリー</li>
                    <li>カメラ</li>
                    <li>飲み物・行動食</li>
                    <li>救急セット(絆創膏など)</li>
                    <li>ウェットティッシュ</li>
                </ul>
            </section>
        </div>
        
        <!-- 部屋割りタブ -->
        <div id="rooms" class="tab-content">
            <section class="section">
                <h2 class="section-title">
                    <span>🏠</span>
                    部屋割り
                </h2>
                
                <div class="room-group">
                    <div class="room-title">🌸 桜の間(4名)</div>
                    <ul class="member-list">
                        <li>田中 太郎(幹事)</li>
                        <li>佐藤 次郎</li>
                        <li>鈴木 三郎</li>
                        <li>高橋 四郎</li>
                    </ul>
                </div>
                
                <div class="room-group">
                    <div class="room-title">🌊 海の間(4名)</div>
                    <ul class="member-list">
                        <li>伊藤 五郎(副幹事)</li>
                        <li>渡辺 六郎</li>
                        <li>山本 七郎</li>
                        <li>中村 八郎</li>
                    </ul>
                </div>
                
                <div class="room-group">
                    <div class="room-title">🏔️ 山の間(4名)</div>
                    <ul class="member-list">
                        <li>小林 九郎</li>
                        <li>加藤 十郎</li>
                        <li>吉田 十一郎</li>
                        <li>山田 十二郎</li>
                    </ul>
                </div>
                
                <div class="room-group">
                    <div class="room-title">🌲 森の間(4名)</div>
                    <ul class="member-list">
                        <li>佐々木 十三郎</li>
                        <li>山口 十四郎</li>
                        <li>松本 十五郎</li>
                        <li>井上 十六郎</li>
                    </ul>
                </div>
            </section>
        </div>
        
        <!-- 注意事項タブ -->
        <div id="notes" class="tab-content">
            <section class="section">
                <h2 class="section-title">
                    <span>⚠️</span>
                    注意事項・ルール
                </h2>
                
                <div class="warning-box">
                    <div class="warning-title">安全に関する注意</div>
                    <ul>
                        <li>ライフジャケットは必ず着用してください(違反者は釣り禁止)</li>
                        <li>飲酒後の釣りは厳禁です</li>
                        <li>単独行動は避け、必ずバディシステムで行動してください</li>
                        <li>天候が悪化した場合は速やかに避難してください</li>
                        <li>体調不良時は無理をせず幹事に報告してください</li>
                    </ul>
                </div>
                
                <div class="warning-box">
                    <div class="warning-title">マナー・ルール</div>
                    <ul>
                        <li>集合時間は厳守してください(遅刻者は置いていきます)</li>
                        <li>釣り場のゴミは必ず持ち帰りましょう</li>
                        <li>他の釣り人や地元の方々への配慮を忘れずに</li>
                        <li>夜間は静かに過ごし、他の宿泊客に迷惑をかけないこと</li>
                        <li>部屋の備品を壊した場合は速やかに報告してください</li>
                        <li>禁煙室での喫煙は厳禁(罰金あり)</li>
                    </ul>
                </div>
                
                <div class="warning-box">
                    <div class="warning-title">その他</div>
                    <ul>
                        <li>キャンセルは3日前まで。それ以降はキャンセル料が発生します</li>
                        <li>貴重品は各自で管理してください(盗難・紛失は自己責任)</li>
                        <li>釣果は記録・撮影後、各自でお持ち帰りください</li>
                        <li>アレルギーがある方は事前に幹事まで連絡してください</li>
                        <li>緊急時は幹事の指示に従ってください</li>
                    </ul>
                </div>
            </section>
            
            <section class="section">
                <h2 class="section-title">
                    <span>🏆</span>
                    大物コンテスト
                </h2>
                <div class="info-grid">
                    <div class="info-item">
                        <span class="info-label">開催日:</span>
                        <span class="info-value">2日目夜 表彰式</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">対象:</span>
                        <span class="info-value">合宿期間中に釣った最大の魚</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">賞品:</span>
                        <span class="info-value">1位:高級ルアーセット、2位:クーラーボックス、3位:釣り雑誌1年分</span>
                    </div>
                    <div class="info-item">
                        <span class="info-label">計測方法:</span>
                        <span class="info-value">全長をメジャーで測定・写真記録必須</span>
                    </div>
                </div>
            </section>
        </div>
        
        <footer class="footer">
            <p>🎣 釣部釣友会 春合宿 2026 🎣</p>
            <p style="margin-top: 10px; font-size: 0.9em;">素晴らしい釣果と思い出を作りましょう!</p>
        </footer>
    </div>
    
    <script>
        // タブ切り替え機能
        function switchTab(event, tabName) {
            // すべてのタブコンテンツを非表示
            const tabContents = document.getElementsByClassName('tab-content');
            for (let content of tabContents) {
                content.classList.remove('active');
            }
            
            // すべてのタブボタンを非アクティブ化
            const tabButtons = document.getElementsByClassName('tab-button');
            for (let button of tabButtons) {
                button.classList.remove('active');
                button.setAttribute('aria-selected', 'false');
            }
            
            // 選択されたタブを表示
            document.getElementById(tabName).classList.add('active');
            event.currentTarget.classList.add('active');
            event.currentTarget.setAttribute('aria-selected', 'true');
            
            // スクロールをトップに戻す
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
        
        // チェックリスト機能
        document.addEventListener('DOMContentLoaded', function() {
            const checklistItems = document.querySelectorAll('.checklist li');
            
            checklistItems.forEach(item => {
                item.addEventListener('click', function() {
                    this.classList.toggle('checked');
                });
            });
        });
        
        // URLハッシュでタブ切り替え
        window.addEventListener('DOMContentLoaded', function() {
            const hash = window.location.hash.substring(1);
            if (hash) {
                const tabButton = document.querySelector(`[onclick*="${hash}"]`);
                if (tabButton) {
                    tabButton.click();
                }
            }
        });
    </script>
</body>
</html>
