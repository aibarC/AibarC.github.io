<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Важность образования в Казахстане</title>
    <style>
        body {
            font-family: Georgia, serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #2c2c2c;
            line-height: 1.6;
        }
        header {
            background-color: #2c3e50;
            color: #fff;
            padding: 20px;
            text-align: center;
        }
        header img {
            height: 50px;
            vertical-align: middle;
        }
        header h1 {
            display: inline-block;
            margin: 0;
            padding-left: 15px;
            font-size: 1.8em;
        }
        main {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background: #ffffff;
            border: 1px solid #ddd;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .section {
            margin-bottom: 30px;
        }
        .section h2 {
            font-size: 1.5em;
            margin-bottom: 10px;
            border-bottom: 2px solid #2c3e50;
            padding-bottom: 5px;
        }
        .tabs {
            display: flex;
            justify-content: space-around;
            margin-bottom: 20px;
            border-bottom: 1px solid #ddd;
        }
        .tab {
            padding: 10px 20px;
            cursor: pointer;
            color: #2c3e50;
            font-weight: bold;
        }
        .tab.active {
            border-bottom: 3px solid #2c3e50;
        }
        .tab-content {
            display: none;
        }
        .tab-content.active {
            display: block;
        }
        .btn {
            display: inline-block;
            padding: 10px 15px;
            background-color: #2c3e50;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #1a242f;
        }
        footer {
            background-color: #2c3e50;
            color: #fff;
            text-align: center;
            padding: 10px;
            font-size: 0.9em;
        }
        form {
            margin-top: 20px;
        }
        form input, form textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 1em;
        }
        form button {
            width: 100%;
            padding: 10px;
            background-color: #2c3e50;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1em;
        }
        form button:hover {
            background-color: #1a242f;
        }
    </style>
</head>
<body>
    <header>
        <img src="logo.png.webl" alt="Logo">
        <h1>Важность образования в Казахстане</h1>
    </header>

    <main>
        <div class="tabs">
            <div class="tab active" data-tab="description">Описание</div>
            <div class="tab" data-tab="registration">Регистрация</div>
        </div>

        <div class="tab-content active" id="description">
            <section class="section">
                <h2>Почему образование важно?</h2>
                <p>Образование играет ключевую роль в развитии общества. В Казахстане оно помогает людям развивать навыки, находить достойные рабочие места и улучшать качество жизни. Узнайте больше о том, как образование способствует инновациям и экономическому росту!</p>
            </section>
        </div>

        <div class="tab-content" id="registration">
            <section class="section">
                <h2>Регистрируйтесь на бесплатные вебинары</h2>
                <p>Участвуйте в наших бесплатных вебинарах, чтобы узнать больше об образовательных возможностях в Казахстане. Просто заполните форму ниже, чтобы зарегистрироваться!</p>

                <form id="webinarForm">
                    <input type="text" placeholder="Ваше имя" required>
                    <input type="email" placeholder="Ваш email" required>
                    <textarea placeholder="Какие темы вас интересуют?" rows="4"></textarea>
                    <button type="submit">Зарегистрироваться</button>
                </form>
            </section>
        </div>

        <section class="section">
            <h2>Дополнительная информация</h2>
            <p>Казахстан стремится стать лидером в области образования в Центральной Азии. Узнайте о новых инициативах, реформах и возможностях для студентов всех возрастов.</p>
            <a href="#" class="btn">Узнать больше</a>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Образовательный Центр Казахстана</p>
    </footer>

    <script>
        const tabs = document.querySelectorAll('.tab');
        const tabContents = document.querySelectorAll('.tab-content');

        tabs.forEach(tab => {
            tab.addEventListener('click', () => {
                tabs.forEach(t => t.classList.remove('active'));
                tabContents.forEach(content => content.classList.remove('active'));

                tab.classList.add('active');
                document.getElementById(tab.dataset.tab).classList.add('active');
            });
        });

        const form = document.getElementById('webinarForm');
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Спасибо за регистрацию! Мы свяжемся с вами по email.');
            form.reset();
        });
    </script>
</body>
</html>
