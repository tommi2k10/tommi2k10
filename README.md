<!DOCTYPE html>
<html lang="vi">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chia Sẻ Câu Chuyện</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            margin: 0;
            padding: 0;
        }
        
        header {
            background-color: #4CAF50;
            color: white;
            padding: 1em 0;
            text-align: center;
        }
        
        main {
            padding: 1em;
        }
        
        .container {
            max-width: 800px;
            margin: auto;
            background-color: white;
            padding: 2em;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        
        .story-form {
            margin-bottom: 2em;
        }
        
        .story-form textarea {
            width: 100%;
            height: 100px;
            padding: 0.5em;
            margin-bottom: 1em;
        }
        
        .story-form button {
            padding: 0.5em 2em;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        
        .story-form button:hover {
            background-color: #45a049;
        }
        
        .story {
            border-bottom: 1px solid #ddd;
            padding: 1em 0;
        }
        
        .story:last-child {
            border-bottom: none;
        }
    </style>
</head>

<body>
    <header>
        <h1>Chia Sẻ Câu Chuyện Của Bạn</h1>
    </header>

    <main>
        <div class="container">
            <section class="story-form">
                <h2>Viết Câu Chuyện Của Bạn</h2>
                <textarea id="storyInput" placeholder="Nhập câu chuyện của bạn ở đây..."></textarea>
                <button onclick="submitStory()">Gửi Câu Chuyện</button>
            </section>

            <section id="stories">
                <h2>Các Câu Chuyện Đã Được Chia Sẻ</h2>
                <!-- Các câu chuyện sẽ được thêm vào đây -->
            </section>
        </div>
    </main>

    <script>
        function submitStory() {
            const storyInput = document.getElementById('storyInput');
            const storyText = storyInput.value.trim();

            if (storyText !== '') {
                const storyContainer = document.createElement('div');
                storyContainer.className = 'story';
                storyContainer.textContent = storyText;

                document.getElementById('stories').appendChild(storyContainer);
                storyInput.value = '';
            } else {
                alert('Vui lòng nhập câu chuyện của bạn!');
            }
        }
    </script>
</body>

</html>
