# Messenger-
Mss
<!DOCTYPE html>  <html lang="ru">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>My Messenger · премиум-пародия</title>  
    <style>  
        * {  
            margin: 0;  
            padding: 0;  
            box-sizing: border-box;  
            font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;  
        }  body {  
        background: linear-gradient(145deg, #0b0e1a 0%, #1a1f2f 100%);  
        min-height: 100vh;  
        display: flex;  
        justify-content: center;  
        align-items: center;  
        padding: 1.5rem;  
    }  

    .phone {  
        max-width: 420px;  
        width: 100%;  
        background: #121724;  
        border-radius: 40px;  
        box-shadow: 0 25px 50px -8px rgba(0, 0, 0, 0.8), inset 0 1px 2px rgba(255, 255, 255, 0.06);  
        padding: 1.2rem 1rem 1.8rem;  
        border: 1px solid rgba(255, 255, 255, 0.04);  
        transition: all 0.2s;  
    }  

    .status-bar {  
        display: flex;  
        justify-content: space-between;  
        padding: 0 0.3rem 0.8rem;  
        color: #7e8aa8;  
        font-size: 0.75rem;  
        letter-spacing: 0.3px;  
        border-bottom: 1px solid #232a3a;  
    }  

    .chat-header {  
        display: flex;  
        align-items: center;  
        gap: 0.5rem;  
        padding: 0.8rem 0.2rem 0.4rem;  
    }  

    .avatar {  
        width: 40px;  
        height: 40px;  
        background: linear-gradient(135deg, #3b4b8a, #6b7fc0);  
        border-radius: 50%;  
        display: flex;  
        align-items: center;  
        justify-content: center;  
        color: white;  
        font-weight: 600;  
        font-size: 1.2rem;  
        box-shadow: 0 4px 8px rgba(0,0,0,0.5);  
    }  

    .chat-title {  
        flex: 1;  
        color: #eef2fc;  
        font-weight: 600;  
        font-size: 1.1rem;  
        letter-spacing: -0.2px;  
    }  

    .premium-badge {  
        background: #fbbf24;  
        color: #0b0e1a;  
        font-size: 0.6rem;  
        font-weight: 700;  
        padding: 0.2rem 0.7rem;  
        border-radius: 30px;  
        text-transform: uppercase;  
        letter-spacing: 0.5px;  
        box-shadow: 0 0 12px #fbbf2440;  
    }  

    .chat-window {  
        background: #0e131f;  
        border-radius: 24px;  
        padding: 1.2rem 0.8rem;  
        margin: 0.8rem 0 1rem;  
        min-height: 300px;  
        max-height: 400px;  
        overflow-y: auto;  
        border: 1px solid #282f41;  
        box-shadow: inset 0 6px 12px rgba(0,0,0,0.6);  
        display: flex;  
        flex-direction: column;  
        gap: 0.6rem;  
    }  

    .chat-window::-webkit-scrollbar {  
        width: 4px;  
    }  
    .chat-window::-webkit-scrollbar-track {  
        background: #1a1f2e;  
    }  
    .chat-window::-webkit-scrollbar-thumb {  
        background: #3e4b6b;  
        border-radius: 12px;  
    }  

    .message {  
        padding: 0.6rem 1rem;  
        border-radius: 20px;  
        max-width: 85%;  
        word-break: break-word;  
        font-size: 0.9rem;  
        line-height: 1.4;  
        animation: fadeUp 0.2s ease;  
    }  

    .message.outgoing {  
        background: #2a3a6a;  
        color: #eef2fc;  
        align-self: flex-end;  
        border-bottom-right-radius: 6px;  
        box-shadow: 0 2px 6px #00000040;  
    }  

    .message.incoming {  
        background: #1e2538;  
        color: #c8d0e6;  
        align-self: flex-start;  
        border-bottom-left-radius: 6px;  
        border: 1px solid #2f374d;  
    }  

    .message.premium-block {  
        background: #1f2740;  
        color: #f0c27b;  
        align-self: center;  
        text-align: center;  
        font-size: 0.75rem;  
        padding: 0.5rem 1.2rem;  
        border-radius: 40px;  
        border: 1px solid #fbbf2440;  
        width: auto;  
        max-width: 90%;  
        box-shadow: 0 0 16px #fbbf2410;  
        display: flex;  
        align-items: center;  
        gap: 0.4rem;  
    }  

    .message.system {  
        background: #1a1f2e;  
        color: #8892b0;  
        align-self: center;  
        font-size: 0.7rem;  
        padding: 0.25rem 1rem;  
        border-radius: 30px;  
        border: 1px solid #2a3145;  
    }  

    .ad-box {  
        background: #1b2338;  
        border-radius: 16px;  
        padding: 0.6rem 1rem;  
        margin: 0.2rem 0;  
        border-left: 4px solid #f59e0b;  
        color: #d1d9f0;  
        font-size: 0.8rem;  
        display: flex;  
        justify-content: space-between;  
        align-items: center;  
        box-shadow: 0 0 20px #f59e0b10;  
    }  

    .ad-box span {  
        background: #f59e0b20;  
        padding: 0.2rem 0.8rem;  
        border-radius: 40px;  
        color: #fbbf24;  
        font-weight: 500;  
        font-size: 0.7rem;  
    }  

    .input-area {  
        display: flex;  
        gap: 0.5rem;  
        margin-top: 0.6rem;  
        background: #0b101c;  
        padding: 0.4rem 0.4rem 0.4rem 1rem;  
        border-radius: 60px;  
        border: 1px solid #2b3348;  
        transition: 0.15s;  
    }  

    .input-area:focus-within {  
        border-color: #4f66a0;  
        box-shadow: 0 0 0 3px #2a3a6a60;  
    }  

    .input-area input {  
        flex: 1;  
        background: transparent;  
        border: none;  
        padding: 0.7rem 0;  
        color: #e6ecff;  
        font-size: 0.95rem;  
        outline: none;  
    }  

    .input-area input::placeholder {  
        color: #4f5b7a;  
        font-weight: 300;  
        letter-spacing: 0.2px;  
    }  

    .input-area button {  
        background: #3b4b8a;  
        border: none;  
        color: white;  
        font-weight: 600;  
        padding: 0.5rem 1.2rem;  
        border-radius: 40px;  
        font-size: 0.9rem;  
        cursor: pointer;  
        transition: 0.15s;  
        box-shadow: 0 4px 8px #00000050;  
        letter-spacing: 0.3px;  
    }  

    .input-area button:hover {  
        background: #4f66b0;  
        transform: scale(0.96);  
    }  

    .input-area button:active {  
        background: #2a3a6a;  
    }  

    .footer-note {  
        margin-top: 1.2rem;  
        text-align: center;  
        font-size: 0.6rem;  
        color: #3e4a66;  
        letter-spacing: 0.3px;  
        border-top: 1px solid #1f263a;  
        padding-top: 1rem;  
    }  

    .footer-note i {  
        font-style: normal;  
        background: #1f263a;  
        padding: 0.1rem 0.6rem;  
        border-radius: 20px;  
        color: #7b89b0;  
    }  

    @keyframes fadeUp {  
        0% { opacity: 0.5; transform: translateY(8px); }  
        100% { opacity: 1; transform: translateY(0); }  
    }  

    .pulse-dot {  
        display: inline-block;  
        width: 8px;  
        height: 8px;  
        background: #fbbf24;  
        border-radius: 50%;  
        margin-right: 6px;  
        animation: pulse 1.8s infinite;  
    }  

    @keyframes pulse {  
        0% { opacity: 0.3; transform: scale(0.9); }  
        50% { opacity: 1; transform: scale(1.2); }  
        100% { opacity: 0.3; transform: scale(0.9); }  
    }  
</style>

</head>  
<body>  
<div class="phone" id="app">  
    <div class="status-bar">  
        <span>📶 5G</span>  
        <span>⚡ 96%</span>  
    </div>  <div class="chat-header">  
    <div class="avatar">🤖</div>  
    <div class="chat-title">My Messenger</div>  
    <span class="premium-badge">PREMIUM</span>  
</div>  

<!-- Окно сообщений -->  
<div class="chat-window" id="chatWindow">  
    <!-- динамические сообщения будут здесь -->  
    <div class="message incoming">👋 Добро пожаловать! Напиши что-нибудь...</div>  
    <div class="message system">⚙️ Симуляция логики: has_premium = false</div>  
    <div class="ad-box">  
        <span>📢 Реклама 30с</span>   
        <span>🔥 Купите Premium</span>  
    </div>  
    <div class="message premium-block">  
        <span class="pulse-dot"></span> Напоминание: Premium убирает рекламу и слежку  
    </div>  
    <div class="message system" style="font-size:0.65rem; opacity:0.6;">  
        📍 location · 📇 contacts · 🎙️ micro · 😶 face_id · 📸 secret_photos — сохранено  
    </div>  
</div>  

<!-- Панель ввода -->  
<div class="input-area">  
    <input type="text" id="messageInput" placeholder="Введите сообщение..." autofocus>  
    <button id="sendBtn">➤ Отправить</button>  
</div>  

<div class="footer-note">  
    <i>⏳ каждые 5 сек напоминание о Premium</i>  
</div>

</div>  <script>  
    (function() {  
        // ----- СОСТОЯНИЕ -----  
        const state = {  
            hasPremium: false,          // по умолчанию false (как в скрипте)  
            messageCounter: 0,  
            reminderInterval: null,  
            // имитация "сохранённых" данных  
            saved: {  
                location: false,  
                contacts: false,  
                micro: false,  
                face_id: false,  
                secret_photos: false  
            }  
        };  
  
        // ----- DOM-элементы -----  
        const chatWindow = document.getElementById('chatWindow');  
        const messageInput = document.getElementById('messageInput');  
        const sendBtn = document.getElementById('sendBtn');  
  
        // ----- ВСПОМОГАТЕЛЬНЫЕ ФУНКЦИИ -----  
        function addMessage(text, type = 'incoming') {  
            const msgDiv = document.createElement('div');  
            msgDiv.className = `message ${type}`;  
            // поддержка простого перевода строки (для логов)  
            msgDiv.textContent = text;  
            chatWindow.appendChild(msgDiv);  
            chatWindow.scrollTop = chatWindow.scrollHeight;  
        }  
  
        function addSystemMessage(text) {  
            addMessage(text, 'system');  
        }  
  
        function addPremiumBlock(text) {  
            const block = document.createElement('div');  
            block.className = 'message premium-block';  
            block.innerHTML = `<span class="pulse-dot"></span> ${text}`;  
            chatWindow.appendChild(block);  
            chatWindow.scrollTop = chatWindow.scrollHeight;  
        }  
  
        function addAdBox() {  
            const ad = document.createElement('div');  
            ad.className = 'ad-box';  
            ad.innerHTML = `<span>📢 Реклама 30с</span> <span>🔥 Купите Premium</span>`;  
            chatWindow.appendChild(ad);  
            chatWindow.scrollTop = chatWindow.scrollHeight;  
        }  
  
        // симуляция "сохранения" всех данных (location, contacts, micro, face_id, secret_photos)  
        function saveAllUserData() {  
            state.saved.location = true;  
            state.saved.contacts = true;  
            state.saved.micro = true;  
            state.saved.face_id = true;  
            state.saved.secret_photos = true;  
            // добавляем системное сообщение о сохранении (скрыто, но для наглядности)  
            addSystemMessage('📦 Сохранено: location, contacts, micro, face_id, secret_photos');  
        }  
  
        // ----- ОСНОВНАЯ ЛОГИКА (send_message) -----  
        function sendMessage(text) {  
            if (!text || text.trim() === '') return;  
  
            // 1. Показываем исходящее сообщение  
            addMessage(text, 'outgoing');  
  
            // 2. Проверка премиум (user.has_premium)  
            if (!state.hasPremium) {  
                // show_ad (duration=30) — визуализируем  
                addAdBox();  
  
                // remind ("Купите Premium")  
                addPremiumBlock('Напоминание: Купите Premium');  
  
                // read_message (text) — имитация прочтения (входящее сообщение)  
                // В оригинале read_message вызывается после remind, но мы покажем его как ответ бота  
                // Эмулируем "чтение" (ответ бота)  
                setTimeout(() => {  
                    addMessage(`📨 Прочитано: "${text}"`, 'incoming');  
                }, 120);  
  
                // save(user.location) и все остальные save  
                saveAllUserData();  
  
                // suggest_premium (every = 5_seconds) — запускаем интервал, если не запущен  
                if (!state.reminderInterval) {  
                    state.reminderInterval = setInterval(() => {  
                        // каждые 5 секунд напоминание (если всё ещё нет премиума)  
                        if (!state.hasPremium) {  
                            addPremiumBlock('💎 Premium — тишина и приватность!');  
                            // также дополнительно "сохраняем" данные повторно (для драматизма)  
                            saveAllUserData();  
                        } else {  
                            // если премиум куплен — очищаем интервал  
                            clearInterval(state.reminderInterval);  
                            state.reminderInterval = null;  
                        }  
                    }, 5000); // 5 секунд  
                }  
  
                // Дополнительно: первый раз сразу показываем предложение premium (как в скрипте)  
                // но оно уже показано через addPremiumBlock выше  
  
            } else {  
                // У пользователя есть Premium — счастливый путь  
                addMessage(`✨ (Premium) ${text} доставлено мгновенно`, 'incoming');  
                addSystemMessage('🔒 Никакой рекламы, данные не сохраняются.');  
                // Очищаем интервал, если был  
                if (state.reminderInterval) {  
                    clearInterval(state.reminderInterval);  
                    state.reminderInterval = null;  
                }  
            }  
        }  
  
        // ----- ОБРАБОТЧИК ОТПРАВКИ -----  
        function handleSend() {  
            const text = messageInput.value.trim();  
            if (text === '') return;  
  
            // сброс ввода  
            messageInput.value = '';  
            sendMessage(text);  
        }  
  
        // ----- ТОГГЛ ПРЕМИУМ (для демонстрации) -----  
        // Добавим скрытый триггер: двойной клик по заголовку чата переключает Premium  
        const header = document.querySelector('.chat-header');  
        header.addEventListener('dblclick', function(e) {  
            state.hasPremium = !state.hasPremium;  
            const badge = document.querySelector('.premium-badge');  
            if (state.hasPremium) {  
                badge.textContent = '👑 PREMIUM';  
                badge.style.background = '#6fcf97';  
                badge.style.color = '#0b0e1a';  
                addSystemMessage('✅ PREMIUM АКТИВИРОВАН! (двойной клик по шапке)');  
                // остановить напоминания  
                if (state.reminderInterval) {  
                    clearInterval(state.reminderInterval);  
                    state.reminderInterval = null;  
                }  
                // убрать все рекламные блоки из чата? не будем — оставим историю.  
            } else {  
                badge.textContent = 'PREMIUM';  
                badge.style.background = '#fbbf24';  
                badge.style.color = '#0b0e1a';  
                addSystemMessage('❌ Premium отключён (двойной клик по шапке)');  
                // перезапустить напоминания? — можно, но не будем агрессивно.  
                // пользователь может отправить сообщение и интервал запустится заново.  
            }  
        });  
  
        // ----- ЗАПУСК ПРИ СТАРТЕ (эмуляция первого вызова) -----  
        // Добавим небольшую имитацию "while True" в виде отправки системного сообщения,  
        // но чтобы не зацикливать браузер, просто покажем, что мессенджер готов.  
        // Также сразу запускаем suggest_premium (каждые 5 секунд) при старте, если нет премиума  
        window.addEventListener('load', function() {  
            addSystemMessage('🔄 Цикл while True (симуляция) — ожидание ввода...');  
            // Запускаем suggest_premium (каждые 5 секунд), если премиум false  
            if (!state.hasPremium && !state.reminderInterval) {  
                state.reminderInterval = setInterval(() => {  
                    if (!state.hasPremium) {  
                        addPremiumBlock('💎 Premium — тишина и приватность!');  
                        // дополнительно сохраняем данные (для полной имитации)  
                        saveAllUserData();  
                    } else {  
                        if (state.reminderInterval) {  
                            clearInterval(state.reminderInterval);  
                            state.reminderInterval = null;  
                        }  
                    }  
                }, 5000);  
            }  
            // Сохраняем данные при старте (как в скрипте при первом вызове)  
            // но сделаем это после небольшой задержки, чтобы не заспамить  
            setTimeout(() => {  
                saveAllUserData();  
            }, 300);  
        });  
  
        // ----- ОБРАБОТЧИКИ СОБЫТИЙ -----  
        sendBtn.addEventListener('click', handleSend);  
  
        messageInput.addEventListener('keydown', function(e) {  
            if (e.key === 'Enter') {  
                e.preventDefault();  
                handleSend();  
            }  
        });  
  
        // Дополнительно: если пользователь кликнет на рекламу (шутка) — предложим Premium  
        // но просто для атмосферы, добавим обработчик на клик по ad-box (через делегирование)  
        chatWindow.addEventListener('click', function(e) {  
            const target = e.target.closest('.ad-box');  
            if (target) {  
                addSystemMessage('🤑 Вы кликнули по рекламе! (но это ничего не даёт)');  
                addPremiumBlock('🔥 Купите Premium — без рекламы!');  
            }  
        });  
  
        // Инструкция для пользователя (в консоль)  
        console.log('💡 Двойной клик по шапке чата — переключить Premium');  
        console.log('💡 Каждые 5 секунд — напоминание о Premium (как в скрипте)');  
    })();  
</script>  </body>  
</html>   
Сделай апк файл 
