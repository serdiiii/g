<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Логово Serdi</title>
<style>
    body {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
        background-color: black;
        color: white;
    }
    #fullscreen-video {
        position: fixed;
        top: 0;
        left: 0;
        min-width: 100%;
        min-height: 100%;
        z-index: -1;
    }
    .content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
    }
    .header {
        font-size: 48px;
        margin-bottom: 20px;
    }
    .button {
        display: inline-block;
        padding: 10px 20px;
        background-color: #ffffff;
        color: #000000;
        text-decoration: none;
        font-size: 24px;
        border-radius: 5px;
        margin: 10px;
    }
</style>
</head>
<body>
    <video id="fullscreen-video" autoplay muted loop>
        <source src="video.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <div class="content">
        <div class="header">Логово Serdi</div>
        <div>Здесь есть многое про меня</div>
        <button class="button" onclick="showChatOptions()">Наш чат</button>
        <a href="information.html" class="button">Информация обо мне</a>
    </div>

    <script>
        function showChatOptions() {
            var choice = prompt("Выберите где общаться: \n1. В общем чате с другими пользователями\n2. С ИИ");
            if (choice === "1") {
                // Редирект на страницу общего чата
                alert("Вы будете перенаправлены на общий чат с другими пользователями.");
                window.location.href = "chat.html";
            } else if (choice === "2") {
                // Редирект на страницу чата с ИИ
                alert("Вы будете перенаправлены на чат с ИИ.");
                window.location.href = "chatii.html";
            } else {
                alert("Пожалуйста, выберите один из вариантов.");
            }
        }
    </script>
</body>
</html>
