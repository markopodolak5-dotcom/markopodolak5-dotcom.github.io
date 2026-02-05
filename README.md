<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHOENIX | DATABASE</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: #0f0f0f; color: #e0e0e0; margin: 0; padding: 0; }
        header { background: #1a1a1a; padding: 15px; text-align: center; border-bottom: 2px solid #ff4444; sticky; top: 0; }
        
        /* Кнопки меню */
        .nav-container { display: flex; justify-content: center; gap: 10px; padding: 10px; background: #111; overflow-x: auto; }
        .nav-btn { background: #222; border: 1px solid #444; color: #fff; padding: 8px 15px; cursor: pointer; border-radius: 5px; white-space: nowrap; }
        .nav-btn:active { background: #ff4444; }

        .content-section { display: none; padding: 20px; animation: fadeIn 0.3s; }
        .active { display: block; }

        h2 { color: #ff4444; border-bottom: 1px solid #333; padding-bottom: 5px; }
        .card { background: #1e1e1e; padding: 15px; border-radius: 8px; margin-bottom: 10px; border-left: 4px solid #ff4444; }
        .advocacy-tips { background: #1a2a1a; border-left-color: #44ff44; padding: 15px; border-radius: 8px; }
        
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

<header>
    <h2 style="margin:0; color: #fff;">PHOENIX LAW</h2>
</header>

<div class="nav-container">
    <button class="nav-btn" onclick="showSection('main')">Главная</button>
    <button class="nav-btn" onclick="showSection('uk')">Уголовный кодекс</button>
    <button class="nav-btn" onclick="showSection('ak')">Административный</button>
    <button class="nav-btn" onclick="showSection('pk')">Процессуальный</button>
</div>

<div id="main" class="content-section active">
    <h2>КАК ДУШИТЬ АДВОКАТА</h2>
    <div class="advocacy-tips">
        <p><b>1. Проверка документов:</b> Требуй удостоверение в развернутом виде. Нет лицухи — гуляй.</p>
        <p><b>2. Время ожидания:</b> Вызвал адвоката? Засекай ровно 10 минут. Ни секундой больше.</p>
        <p><b>3. Конфиденциальная беседа:</b> Если он требует 15 минут, следи, чтобы не передал ничего задержанному.</p>
        <p><i>(Сюда добавим твои коронные методы, когда напишешь)</i></p>
    </div>
</div>

<div id="uk" class="content-section">
    <h2>УГОЛОВНЫЙ КОДЕКС</h2>
    <div class="card">
        <b>Статья 12.8</b><br>
        Незаконное оружие. До 50 месяцев.
    </div>
    </div>

<div id="ak" class="content-section">
    <h2>АДМИНИСТРАТИВНЫЙ КОДЕКС</h2>
    <div class="card">
        <b>Статья 1.1</b><br>
        Нарушение дорожного кодекса. Штраф.
    </div>
</div>

<div id="pk" class="content-section">
    <h2>ПРОЦЕССУАЛЬНЫЙ КОДЕКС</h2>
    <div class="card">
        1. Наручники -> 2. Жетон -> 3. Миранда.
    </div>
</div>

<script>
    function showSection(id) {
        // Скрываем все секции
        document.querySelectorAll('.content-section').forEach(s => s.classList.remove('active'));
