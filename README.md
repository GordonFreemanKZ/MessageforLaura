<!doctype html>
<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Радужная страница для большого текста</title>
  <style>
    html,body{height:100%;margin:0}
    body{
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji";
      line-height:1.6;
      background: linear-gradient(120deg, #ff0066, #ff9900, #ffee00, #33cc33, #00bbff, #6633ff, #cc00ff, #ff0066);
      background-size: 600% 600%;
      animation: rainbow 18s ease infinite;
      min-height:100%;
    }
    @keyframes rainbow{
      0%{background-position:0% 50%}
      50%{background-position:100% 50%}
      100%{background-position:0% 50%}
    }
    .sheet{
      width:min(1200px, 92vw);
      margin: 2rem auto;
      padding: clamp(16px, 2vw, 32px);
      border-radius: 24px;
      background: rgba(255,255,255,0.88);
      color: #111;
      box-shadow: 0 20px 60px rgba(0,0,0,.25);
      backdrop-filter: blur(10px) saturate(120%);
    }
    @media (prefers-color-scheme: dark){
      .sheet{ background: rgba(0,0,0,0.55); color: #f4f4f4 }
    }
    h1{
      margin:0 0 .6rem 0; font-size: clamp(1.4rem, 1.6rem + 1vw, 2.2rem);
    }
    .hint{opacity:.8; font-size:.95rem; margin-bottom:1rem}
    #editor{
      min-height: 70vh;
      outline: none;
      white-space: pre-wrap;
      word-wrap: break-word;
      overflow-wrap: anywhere;
      font-size: clamp(16px, 1rem + .3vw, 20px);
      line-height: 1.7;
    }
    #editor:empty:before{
      content: 'Вставьте или напечатайте ваш текст здесь…';
      opacity:.55;
    }
  </style>
</head>
<body>
  <main class="sheet" role="main" aria-label="Текстовый лист">
    <h1>Лаура, мой номер телефона +77470724110</h1>
  </main>
</body>
</html>
