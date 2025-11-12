<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ name }} haqidagi sahifa</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f5f5f5;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 80%;
            margin: 30px auto;
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #007BFF;
        }
        ul {
            list-style: none;
            padding: 0;
        }
        li {
            background: #e9f1ff;
            margin: 5px 0;
            padding: 8px;
            border-radius: 5px;
        }
        .contact a {
            color: #007BFF;
            text-decoration: none;
        }
        .contact a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>{{ name }} haqida</h1>
        <p>{{ about }}</p>

        <h2>Qiziqishlarim</h2>
        <ul>
            {% for hobby in hobbies %}
                <li>{{ hobby }}</li>
            {% endfor %}
        </ul>

        <h2>Bog‘lanish</h2>
        <div class="contact">
            <p>Email: {{ contact.Email }}</p>
            <p>Telegram: {{ contact.Telegram }}</p>
            <p>GitHub: <a href="{{ contact.GitHub }}" target="_blank">{{ contact.GitHub }}</a></p>
        </div>
    </div>
</body>
</html>
