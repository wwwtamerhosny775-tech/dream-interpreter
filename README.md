<meta name='viewport' content='width=device-width, initial-scale=1'/><!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>عبدالقادر عصام حسن محمد | AR AI</title>
    <style>
        /* ===== RESET & BASE ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(145deg, #0b0e1a 0%, #141a2b 100%);
            color: #e8edf5;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        /* ===== MAIN CONTAINER ===== */
        .app-container {
            max-width: 1200px;
            width: 100%;
            background: rgba(22, 30, 50, 0.85);
            backdrop-filter: blur(14px);
            -webkit-backdrop-filter: blur(14px);
            border-radius: 48px;
            padding: 30px 35px 40px;
            box-shadow: 0 25px 60px rgba(0, 0, 0, 0.8), inset 0 0 0 1px rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(255, 255, 255, 0.03);
            transition: all 0.3s ease;
        }

        /* ===== HEADER ===== */
        .header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 28px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            padding-bottom: 20px;
        }

        .brand {
            display: flex;
            align-items: center;
            gap: 14px;
        }

        .brand-icon {
            width: 56px;
            height: 56px;
            background: linear-gradient(135deg, #00c9ff, #92fe9d);
            border-radius: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 900;
            font-size: 24px;
            color: #0b0e1a;
            box-shadow: 0 8px 20px rgba(0, 201, 255, 0.25);
        }

        .brand h1 {
            font-size: 24px;
            font-weight: 700;
            background: linear-gradient(135deg, #f0f9ff, #b6d4ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.3px;
        }

        .brand .sub {
            font-size: 14px;
            color: #8da4d0;
            -webkit-text-fill-color: #8da4d0;
            font-weight: 400;
            letter-spacing: 0.3px;
        }

        .contact-badge {
            background: rgba(0, 201, 255, 0.10);
            border: 1px solid rgba(0, 201, 255, 0.20);
            padding: 10px 22px;
            border-radius: 60px;
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 15px;
            transition: 0.3s;
            backdrop-filter: blur(6px);
        }

        .contact-badge:hover {
            background: rgba(0, 201, 255, 0.18);
            border-color: rgba(0, 201, 255, 0.45);
            transform: scale(1.02);
        }

        .contact-badge .phone {
            color: #b6d4ff;
            font-weight: 600;
            letter-spacing: 0.5px;
        }

        .contact-badge .label {
            color: #8da4d0;
            font-weight: 300;
        }

        /* ===== LAYOUT: CHAT + SIDEBAR ===== */
        .main-grid {
            display: grid;
            grid-template-columns: 1fr 320px;
            gap: 30px;
        }

        /* ===== CHAT AREA ===== */
        .chat-panel {
            background: rgba(12, 18, 34, 0.55);
            border-radius: 32px;
            padding: 22px 24px 20px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            box-shadow: inset 0 4px 20px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            min-height: 520px;
        }

        .chat-messages {
            flex: 1;
            overflow-y: auto;
            max-height: 460px;
            padding-left: 6px;
            margin-bottom: 18px;
            scroll-behavior: smooth;
        }

        .chat-messages::-webkit-scrollbar {
            width: 5px;
        }
        .chat-messages::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 10px;
        }
        .chat-messages::-webkit-scrollbar-thumb {
            background: #2f3f6a;
            border-radius: 10px;
        }

        .message {
            margin-bottom: 18px;
            display: flex;
            flex-direction: column;
        }

        .message.user {
            align-items: flex-end;
        }

        .message.ai {
            align-items: flex-start;
        }

        .bubble {
            max-width: 88%;
            padding: 14px 20px;
            border-radius: 24px;
            line-height: 1.7;
            font-size: 15px;
            word-wrap: break-word;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            animation: fadeSlide 0.3s ease;
        }

        .message.user .bubble {
            background: linear-gradient(135deg, #1f8ef1, #3b9eff);
            color: #fff;
            border-bottom-right-radius: 6px;
        }

        .message.ai .bubble {
            background: rgba(32, 44, 72, 0.75);
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.06);
            color: #e0ebff;
            border-bottom-left-radius: 6px;
        }

        .bubble .msg-label {
            font-size: 11px;
            font-weight: 600;
            opacity: 0.6;
            margin-bottom: 4px;
            letter-spacing: 0.3px;
        }

        .bubble ul {
            margin: 8px 0 4px 18px;
            padding-right: 6px;
        }
        .bubble ul li {
            margin-bottom: 4px;
        }

        /* ===== INPUT ===== */
        .input-row {
            display: flex;
            gap: 12px;
            align-items: center;
            background: rgba(18, 26, 48, 0.7);
            border-radius: 60px;
            padding: 6px 6px 6px 18px;
            border: 1px solid rgba(255, 255, 255, 0.07);
            backdrop-filter: blur(6px);
            transition: 0.25s;
        }

        .input-row:focus-within {
            border-color: rgba(0, 201, 255, 0.35);
            box-shadow: 0 0 0 4px rgba(0, 201, 255, 0.07);
        }

        .input-row input {
            flex: 1;
            background: transparent;
            border: none;
            padding: 14px 6px;
            color: #e8edf5;
            font-size: 15px;
            outline: none;
        }

        .input-row input::placeholder {
            color: #5f73a0;
            font-weight: 300;
        }

        .input-row button {
            background: linear-gradient(135deg, #00c9ff, #1f8ef1);
            border: none;
            color: #0b0e1a;
            font-weight: 700;
            padding: 12px 28px;
            border-radius: 60px;
            font-size: 15px;
            cursor: pointer;
            transition: 0.25s;
            display: flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 6px 18px rgba(0, 201, 255, 0.20);
            letter-spacing: 0.3px;
        }

        .input-row button:hover {
            transform: scale(1.03);
            box-shadow: 0 8px 28px rgba(0, 201, 255, 0.35);
        }

        .input-row button:active {
            transform: scale(0.97);
        }

        /* ===== SIDEBAR ===== */
        .sidebar {
            display: flex;
            flex-direction: column;
            gap: 24px;
        }

        .profile-card {
            background: rgba(12, 18, 34, 0.60);
            border-radius: 32px;
            padding: 28px 22px 24px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            text-align: center;
            backdrop-filter: blur(6px);
        }

        .avatar {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, #00c9ff, #92fe9d);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 44px;
            font-weight: 900;
            color: #0b0e1a;
            margin: 0 auto 16px;
            box-shadow: 0 12px 30px rgba(0, 201, 255, 0.20);
        }

        .profile-card h2 {
            font-size: 20px;
            font-weight: 700;
            margin-bottom: 4px;
            background: linear-gradient(135deg, #f0f9ff, #b6d4ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .profile-card .tag {
            color: #8da4d0;
            font-size: 14px;
            font-weight: 400;
            margin-bottom: 14px;
        }

        .profile-card .bio {
            font-size: 14px;
            line-height: 1.8;
            color: #b6c8ee;
            text-align: right;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            padding-top: 16px;
            margin-top: 6px;
        }

        .quick-actions {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .quick-actions button {
            background: rgba(32, 44, 72, 0.55);
            border: 1px solid rgba(255, 255, 255, 0.05);
            padding: 14px 18px;
            border-radius: 20px;
            color: #c8d8ff;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.2s;
            text-align: right;
            backdrop-filter: blur(4px);
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .quick-actions button:hover {
            background: rgba(0, 201, 255, 0.10);
            border-color: rgba(0, 201, 255, 0.20);
            transform: translateX(-4px);
        }

        .quick-actions button .emoji {
            font-size: 20px;
            width: 30px;
            text-align: center;
        }

        /* ===== PROJECTS SECTION ===== */
        .projects-section {
            background: rgba(12, 18, 34, 0.60);
            border-radius: 32px;
            padding: 22px 20px 20px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            backdrop-filter: blur(6px);
        }

        .projects-section h3 {
            font-size: 17px;
            font-weight: 600;
            color: #b6d4ff;
            margin-bottom: 14px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .project-item {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 16px;
            padding: 14px 16px;
            margin-bottom: 12px;
            border-right: 3px solid rgba(0, 201, 255, 0.30);
            transition: 0.2s;
        }

        .project-item:hover {
            background: rgba(255, 255, 255, 0.06);
            border-right-color: #00c9ff;
        }

        .project-item .title {
            font-weight: 600;
            color: #e0ebff;
            font-size: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .project-item .desc {
            font-size: 13px;
            color: #8da4d0;
            margin-top: 4px;
            line-height: 1.6;
        }

        .project-item .status {
            display: inline-block;
            font-size: 11px;
            background: rgba(0, 201, 255, 0.12);
            color: #8da4d0;
            padding: 2px 12px;
            border-radius: 30px;
            margin-top: 6px;
        }

        /* ===== FOOTER ===== */
        .footer {
            margin-top: 30px;
            padding-top: 18px;
            border-top: 1px solid rgba(255, 255, 255, 0.04);
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            font-size: 13px;
            color: #4d628a;
        }

        .footer span {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer .highlight {
            color: #8da4d0;
        }

        /* ===== ANIMATIONS ===== */
        @keyframes fadeSlide {
            0% {
                opacity: 0;
                transform: translateY(10px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .typing-indicator {
            display: inline-flex;
            gap: 6px;
            padding: 6px 12px;
            background: rgba(32, 44, 72, 0.5);
            border-radius: 30px;
            margin-top: 6px;
        }

        .typing-indicator span {
            width: 10px;
            height: 10px;
            background: #8da4d0;
            border-radius: 50%;
            display: inline-block;
            animation: wave 1.4s infinite ease-in-out both;
        }

        .typing-indicator span:nth-child(1) {
            animation-delay: -0.32s;
        }
        .typing-indicator span:nth-child(2) {
            animation-delay: -0.16s;
        }
        .typing-indicator span:nth-child(3) {
            animation-delay: 0s;
        }

        @keyframes wave {
            0%,
            80%,
            100% {
                transform: scale(0.6);
                opacity: 0.4;
            }
            40% {
                transform: scale(1);
                opacity: 1;
            }
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 900px) {
            .main-grid {
                grid-template-columns: 1fr;
            }
            .app-container {
                padding: 20px;
            }
            .header {
                flex-direction: column;
                align-items: flex-start;
                gap: 14px;
            }
            .contact-badge {
                width: 100%;
                justify-content: center;
            }
            .brand h1 {
                font-size: 20px;
            }
        }

        @media (max-width: 480px) {
            .bubble {
                max-width: 96%;
                font-size: 14px;
                padding: 12px 16px;
            }
            .input-row {
                flex-wrap: wrap;
                background: transparent;
                padding: 0;
                gap: 8px;
                border: none;
            }
            .input-row input {
                background: rgba(18, 26, 48, 0.8);
                border-radius: 60px;
                padding: 14px 18px;
                width: 100%;
                border: 1px solid rgba(255, 255, 255, 0.07);
            }
            .input-row button {
                width: 100%;
                justify-content: center;
                padding: 14px;
            }
            .sidebar .quick-actions button {
                font-size: 13px;
                padding: 12px 14px;
            }
        }
    </style>
</head>
<body>
    <div class="app-container" id="app">
        <!-- HEADER -->
        <header class="header">
            <div class="brand">
                <div class="brand-icon">AR</div>
                <div>
                    <h1>عبدالقادر <span class="sub">AI</span></h1>
                    <div style="font-size:13px; color:#6f87b5; margin-top:2px;">ذكاء اصطناعي شخصي</div>
                </div>
            </div>
            <div class="contact-badge">
                <span class="label">📱 تواصل</span>
                <span class="phone" id="phoneDisplay">775800699</span>
                <button onclick="copyPhone()" style="background:transparent;border:none;color:#8da4d0;cursor:pointer;font-size:18px;" title="انسخ الرقم">📋</button>
            </div>
        </header>

        <!-- MAIN GRID -->
        <div class="main-grid">
            <!-- CHAT -->
            <section class="chat-panel">
                <div class="chat-messages" id="chatMessages">
                    <!-- الرسائل تظهر هنا بواسطة JavaScript -->
                </div>

                <div class="input-row">
                    <input type="text" id="userInput" placeholder="اكتب سؤالك عن عبدالقادر..." />
                    <button id="sendBtn">إرسال ✦</button>
                </div>
                <div style="display:flex; gap:8px; margin-top:12px; flex-wrap:wrap;">
                    <button class="quick-chip" data-msg="من هو عبدالقادر؟">👤 من هو؟</button>
                    <button class="quick-chip" data-msg="ما هي مهارات عبدالقادر؟">⚡ المهارات</button>
                    <button class="quick-chip" data-msg="معلومات">📚 كل المعلومات</button>
                    <button class="quick-chip" data-msg="رقم التواصل">📞 رقم التواصل</button>
                    <button class="quick-chip" data-msg="ما هي مشاريع عبدالقادر؟">🚀 المشاريع</button>
                </div>
            </section>

            <!-- SIDEBAR -->
            <aside class="sidebar">
                <div class="profile-card">
                    <div class="avatar">AR</div>
                    <h2>عبدالقادر عصام حسن محمد</h2>
                    <div class="tag">🇾🇪 يمني · مختص تقني وإداري</div>
                    <div class="bio">
                        يجمع بين إدارة الأعمال، البرمجة، الأمن السيبراني، صيانة الهواتف، الذكاء الاصطناعي، وريادة الأعمال.<br />
                        <span style="display:inline-block; margin-top:8px; background:rgba(0,201,255,0.08); padding:4px 14px; border-radius:30px; font-size:12px; color:#8da4d0;">🏷️ الهوية الرقمية: AR</span>
                    </div>
                </div>

                <div class="quick-actions">
                    <button onclick="askQuick('معلومات عن تخصصات عبدالقادر')">
                        <span class="emoji">🧩</span> التخصصات
                    </button>
                    <button onclick="askQuick('ما هي مشاريع عبدالقادر؟')">
                        <span class="emoji">🚀</span> المشاريع
                    </button>
                    <button onclick="askQuick('ما هي رؤية عبدالقادر المهنية؟')">
                        <span class="emoji">🎯</span> الرؤية المهنية
                    </button>
                    <button onclick="askQuick('ما هي اهتمامات عبدالقادر البحثية؟')">
                        <span class="emoji">🔬</span> الاهتمامات البحثية
                    </button>
                    <button onclick="askQuick('ما هي المجالات المهنية لعبدالقادر؟')">
                        <span class="emoji">📂</span> المجالات المهنية
                    </button>
                    <button onclick="askQuick('ما هو المسار التطويري لعبدالقادر؟')">
                        <span class="emoji">🛤️</span> المسار التطويري
                    </button>
                    <button onclick="askQuick('ما هي فلسفة عمل عبدالقادر؟')">
                        <span class="emoji">💡</span> فلسفة العمل
                    </button>
                </div>

                <!-- ===== PROJECTS SECTION ===== -->
                <div class="projects-section">
                    <h3>🚀 مشاريعي الخاصة</h3>
                    <div id="projectsList">
                        <!-- يتم تعبئتها بواسطة JavaScript -->
                    </div>
                </div>
            </aside>
        </div>

        <!-- FOOTER -->
        <div class="footer">
            <span>🧠 <span class="highlight">ذكاء عبدالقادر الاصطناعي</span> · قاعدة معرفية شاملة بدون تكرار</span>
            <span>📱 <span class="highlight" id="footerPhone">775800699</span></span>
        </div>
    </div>

    <script>
        // ============================================================
        //  BASE KNOWLEDGE (معلومات شاملة + المعلومات الجديدة)
        // ==================================================
