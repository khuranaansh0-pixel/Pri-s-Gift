# Pri-s-Gift
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>priashi's lil corner ♡</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }
        
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .star {
            position: absolute;
            background: rgba(255,255,255,0.8);
            border-radius: 50%;
            animation: twinkle 3s infinite ease-in-out;
        }
        
        @keyframes twinkle {
            0%, 100% { opacity: 0.3; transform: scale(0.8); }
            50% { opacity: 1; transform: scale(1.2); }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 10;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
            animation: slideInDown 1s ease-out;
        }
        
        .title {
            font-size: clamp(2.5rem, 8vw, 5rem);
            font-weight: 700;
            background: linear-gradient(45deg, #ff9a9e, #fecfef, #fecfef, #ff9a9e);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradientShift 3s ease infinite, float 6s ease-in-out infinite;
            margin-bottom: 10px;
            text-shadow: 0 4px 20px rgba(255,154,158,0.3);
        }
        
        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        
        @keyframes slideInDown {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        .subtitle {
            font-size: clamp(1rem, 3vw, 1.5rem);
            color: rgba(255,255,255,0.9);
            font-weight: 300;
            letter-spacing: 2px;
        }
        
        .messages {
            flex: 1;
            max-height: 70vh;
            overflow-y: auto;
            padding: 20px;
            scrollbar-width: thin;
            scrollbar-color: rgba(255,255,255,0.3) transparent;
            margin-bottom: 30px;
        }
        
        .messages::-webkit-scrollbar {
            width: 6px;
        }
        
        .messages::-webkit-scrollbar-track {
            background: transparent;
        }
        
        .messages::-webkit-scrollbar-thumb {
            background: rgba(255,255,255,0.3);
            border-radius: 3px;
        }
        
        .message-bubble {
            margin-bottom: 20px;
            opacity: 0;
            transform: translateY(30px);
            animation: slideInUp 0.6s ease-out forwards;
        }
        
        .message-bubble:nth-child(even) { animation-delay: 0.1s; }
        .message-bubble:nth-child(odd) { animation-delay: 0.2s; }
        
        @keyframes slideInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .message {
            max-width: 80%;
            padding: 16px 20px;
            border-radius: 24px;
            box-shadow: 0 8px 32px rgba(0,0,0,0.1);
            position: relative;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
        }
        
        .message.priashi {
            background: linear-gradient(135deg, rgba(255,255,255,0.95), rgba(255,255,255,0.85));
            color: #333;
            margin-left: auto;
            border-radius: 24px 24px 8px 24px;
        }
        
        .message.ansh {
            background: linear-gradient(135deg, rgba(255,154,158,0.95), rgba(254,207,239,0.9));
            color: #333;
            margin-right: auto;
            border-radius: 24px 24px 24px 8px;
        }
        
        .sender {
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 8px;
            opacity: 0.8;
        }
        
        .sender.priashi { color: #ff6b9d; }
        .sender.ansh { color: #ff8fab; }
        
        .content {
            font-size: 1rem;
            line-height: 1.5;
            white-space: pre-wrap;
        }
        
        .timestamp {
            font-size: 0.75rem;
            opacity: 0.6;
            margin-top: 8px;
            text-align: right;
        }
        
        .contact-section {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(20px);
            border-radius: 24px;
            padding: 30px;
            margin: 30px 0;
            border: 1px solid rgba(255,255,255,0.2);
            animation: fadeInUp 1s ease-out 0.5s both;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .section-title {
            font-size: 1.8rem;
            font-weight: 600;
            text-align: center;
            margin-bottom: 25px;
            background: linear-gradient(45deg, #ff9a9e, #fecfef);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .email-form {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .form-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }
        
        .form-group label {
            font-size: 0.9rem;
            font-weight: 500;
            color: rgba(255,255,255,0.9);
        }
        
        .form-group input,
        .form-group textarea {
            padding: 15px 20px;
            border: 2px solid rgba(255,255,255,0.2);
            border-radius: 16px;
            background: rgba(255,255,255,0.9);
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #ff9a9e;
            box-shadow: 0 0 0 3px rgba(255,154,158,0.2);
            transform: translateY(-2px);
        }
        
        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }
        
        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 50px;
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            justify-content: center;
        }
        
        .btn-primary {
            background: linear-gradient(45deg, #ff9a9e, #fecfef);
            color: #fff;
            box-shadow: 0 8px 32px rgba(255,154,158,0.4);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 40px rgba(255,154,158,0.6);
        }
        
        .btn-whatsapp {
            background: linear-gradient(45deg, #25D366, #128C7E);
            color: #fff;
            box-shadow: 0 8px 32px rgba(37,211,102,0.4);
            margin-top: 15px;
        }
        
        .btn-whatsapp:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 40px rgba(37,211,102,0.6);
        }
        
        .btns-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
            align-items: center;
        }
        
        .success-msg {
            background: linear-gradient(135deg, #10b981, #059669);
            color: white;
            padding: 15px 20px;
            border-radius: 16px;
            text-align: center;
            margin-top: 15px;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.4s ease;
        }
        
        .success-msg.show {
            opacity: 1;
            transform: translateY(0);
        }
        
        @media (max-width: 768px) {
            .container { padding: 15px; }
            .messages { padding: 15px; max-height: 60vh; }
            .message { max-width: 90%; padding: 14px 18px; }
            .contact-section { padding: 20px; margin: 20px 0; }
        }
        
        @media (max-width: 480px) {
            .title { font-size: 2.5rem; }
            .message { max-width: 95%; }
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>
    
    <div class="container">
        <div class="header">
            <h1 class="title">priashi's lil corner ♡</h1>
            <p class="subtitle">our lil memories, forever 💕</p>
        </div>
        
        <div class="messages" id="messages">
            <div class="message-bubble">
                <div class="message priashi">
                    <div class="sender priashi">priashi</div>
                    <div class="content">lmao</div>
                    <div class="timestamp">Nov 25, 2025 12:31 am</div>
                </div>
            </div>
            <div class="message-bubble">
                <div class="message ansh">
                    <div class="sender ansh">Ansh Khurana</div>
                    <div class="content">Hehe</div>
                    <div class="timestamp">Nov 25, 2025 12:29 am</div>
                </div>
            </div>
            <div class="message-bubble">
                <div class="message ansh">
                    <div class="sender ansh">Ansh Khurana</div>
                    <div class="content">Well.. mostly yourself!!</div>
                    <div class="timestamp">Nov 25, 2025 12:29 am</div>
                </div>
            </div>
            <div class="message-bubble">
                <div class="message priashi">
                    <div class="sender priashi">priashi</div>
                    <div class="content">what do you think 😉</div>
                    <div class="timestamp">Nov 25, 2025 12:23 am</div>
                </div>
            </div>
            <div class="message-bubble">
                <div class="message ansh">
                    <div class="sender ansh">Ansh Khurana</div>
                    <div class="content">What's distracting you? 🤭</div>
                    <div class="timestamp">Nov 25, 2025 12:03 am</div>
                </div>
            </div>
            <div class="message-bubble">
                <div class="message priashi">
                    <div class="sender priashi">priashi</div>
                    <div class="content">❤ Ansh Khurana</div>
                    <div class="timestamp">Nov 24, 2025 11:34 pm</div>
                </div>
            </div>
            <div class="message-bubble">
                <div class="message priashi">
                    <div class="sender priashi">priashi</div>
                    <div class="content">Liked a message</div>
                    <div class="timestamp">Nov 24, 2025 11:33 pm</div>
                </div>
            </div>
            <div class="message-bubble">
                <div class="message ansh">
                    <div class="sender ansh">Ansh Khurana</div>
                    <div class="content">❤ priashi</div>
                    <div class="timestamp">Nov 24, 2025 11:11 pm</div>
                </div>
            </div>
        </div>
        
        <div class="contact-section">
            <h2 class="section-title">miss me already? ♡</h2>
            
            <form class="email-form" id="emailForm">
                <div class="form-group">
                    <label for="email">your email 💌</label>
                    <input type="email" id="email" name="email" required placeholder="priashi@gmail.com">
                </div>
                
                <div class="form-group">
                    <label for="message">what u thinking? how's home? 🏠</label>
                    <textarea id="message" name="message" required placeholder="tell me everything... i've missed you ♡"></textarea>
                </div>
                
                <div class="btns-container">
                    <button type="submit" class="btn btn-primary">send to ansh ♡</button>
                    <a href="https://wa.me/917027641015?text=Hey%20Ansh!%20Just%20saw%20your%20lil%20corner...%20missed%20you%20💕" class="btn btn-whatsapp" target="_blank">text ansh now 📱</a>
                </div>
            </form>
            
            <div class="success-msg" id="successMsg">sent with love! ansh will reply soon ♡</div>
        </div>
    </div>

    <script>
        function createStars() {
            const starsContainer = document.getElementById('stars');
            for (let i = 0; i < 100; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.width = star.style.height = (Math.random() * 3 + 1) + 'px';
                star.style.animationDelay = Math.random() * 3 + 's';
                star.style.animationDuration = (Math.random() * 3 + 2) + 's';
                starsContainer.appendChild(star);
            }
        }

        document.getElementById('emailForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const successMsg = document.getElementById('successMsg');
            successMsg.classList.add('show');
            setTimeout(() => {
                successMsg.classList.remove('show');
                this.reset();
            }, 4000);
            document.querySelector('.messages').scrollTop = 0;
        });

        window.addEventListener('load', function() {
            createStars();
            setTimeout(() => {
                document.getElementById('messages').scrollTop = document.getElementById('messages').scrollHeight;
            }, 1000);
        });
    </script>
</body>
</html>
