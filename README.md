
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>你点进来啦！</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffcccb;
            font-family: 'Comic Sans MS', cursive, sans-serif;
            overflow: hidden;
        }

        .container {
            text-align: center;
            position: relative;
        }

        h1 {
            font-size: 3rem;
            color: #ff69b4;
            animation: bounce 2s infinite;
        }

        .pig {
            font-size: 10rem;
            animation: spin 4s linear infinite, float 3s ease-in-out infinite;
        }

        .hidden-text {
            font-size: 1.5rem;
            color: #ff69b4;
            margin-top: 20px;
            opacity: 0;
            animation: fadeIn 5s forwards;
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        @keyframes spin {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>你点进来啦！</h1>
        <div class="pig">🐷</div>
        <div class="hidden-text">哈哈，你是可爱的小猪！</div>
    </div>

    <script>
        // 添加音效
        const audio = new Audio('https://www.soundjay.com/button/sounds/button-3.mp3');
        audio.play();

        // 点击页面任何地方都会弹出提示
        document.body.addEventListener('click', () => {
            alert('哼哼，小猪你好呀！');
        });
    </script>
</body>
</html>
