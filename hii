<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ИНФО САЙТ</title>
<meta name="description" content="Личная страница в стиле 2007–2010: блёстки, гифки, музыка, ник, ссылки." />

<!-- 2007–2010 AESTHETIC: lots of gradients, bevels, drop-shadows, marquee, visitor counter mock, gif zone -->
<style>
  /* RESET-ish */
  * { box-sizing: border-box; }

  /* BACKGROUND: tiled glitter feel via layered gradients */
  body {
    margin: 0;
    background:
      radial-gradient(circle at 10% 10%, rgba(255,255,255,.25), transparent 40%),
      radial-gradient(circle at 90% 20%, rgba(255,255,255,.18), transparent 40%),
      radial-gradient(circle at 30% 80%, rgba(255,255,255,.22), transparent 40%),
      linear-gradient(135deg, #00e0ff 0%, #00b4ff 20%, #7a00ff 60%, #ff008c 100%);
    background-attachment: fixed;
    font-family: "Trebuchet MS", Tahoma, Verdana, Arial, sans-serif;
    color: #fff;
    text-shadow: 0 1px 1px rgba(0,0,0,.4);
    cursor: url('data:image/svg+xml;utf8,\
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32">\
        <circle cx="8" cy="8" r="3" fill="white"/>\
      </svg>') 2 2, auto;
  }

  /* PAGE WRAPPER: fixed width like old sites */
  .wrap {
    width: 980px;
    max-width: 100%;
    margin: 20px auto 60px;
    padding: 12px;
  }

  /* HEADER with shiny bevel + glow */
  .header {
    border: 3px solid rgba(255,255,255,.7);
    border-radius: 10px;
    background: linear-gradient(#1a1a1a, #111) padding-box,
                linear-gradient(145deg, rgba(255,255,255,.6), rgba(255,255,255,.1)) border-box;
    box-shadow: 0 8px 25px rgba(0,0,0,.6), inset 0 1px 0 rgba(255,255,255,.15);
    padding: 18px;
    position: relative;
    overflow: hidden;
  }

  /* "Shine" sweep */
  .header::after {
    content: "";
    position: absolute;
    top: -50%;
    left: -20%;
    width: 40%;
    height: 200%;
    transform: rotate(25deg);
    background: linear-gradient( to right,
      rgba(255,255,255,0) 0%,
      rgba(255,255,255,.35) 45%,
      rgba(255,255,255,0) 60%);
    animation: sweep 4.5s linear infinite;
    pointer-events: none;
  }
  @keyframes sweep { 
    0% { left: -40%; } 
    100% { left: 120%; } 
  }

  /* BIG NICKNAME */
  .nickname {
    font-family: "Comic Sans MS", "Comic Sans", cursive;
    font-size: clamp(40px, 7vw, 86px);
    letter-spacing: 2px;
    text-align: center;
    margin: 0;
    color: #ffdbff;
    text-shadow:
      0 0 8px #ff43f3,
      0 0 16px #a300ff,
      1px 2px 0 rgba(0,0,0,.6);
  }

  /* marquee strip like 2008 */
  .ticker {
    margin-top: 12px;
    border-top: 1px dotted rgba(255,255,255,.35);
    border-bottom: 1px dotted rgba(255,255,255,.35);
    background: rgba(0,0,0,.35);
    padding: 6px 0;
    font-size: 14px;
    white-space: nowrap;
  }
  .ticker small { opacity: .9; }

  /* NAV buttons — glossy gradients + hard bevel */
  .nav {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: center;
    margin: 18px 0 0;
  }
  .btn {
    display: inline-block;
    padding: 10px 16px;
    border-radius: 6px;
    border: 2px solid rgba(255,255,255,.7);
    background: linear-gradient(#ff62c2, #e40075);
    box-shadow:
      inset 0 1px 0 rgba(255,255,255,.55),
      inset 0 -3px 0 rgba(0,0,0,.3),
      0 6px 12px rgba(0,0,0,.45);
    color: #fff; text-decoration: none; font-weight: bold;
    text-shadow: 0 1px 0 rgba(0,0,0,.5);
    transition: transform .05s ease-in-out;
  }
  .btn:hover { transform: translateY(-1px); }
  .btn:active { transform: translateY(1px); box-shadow: inset 0 2px 6px rgba(0,0,0,.55); }

  /* CONTENT PANELS (like tables & boxes from old forums) */
  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-top: 18px;
  }
  @media (max-width: 820px){ .grid { grid-template-columns: 1fr; } }

  .panel {
    background: rgba(0,0,0,.45);
    border: 3px ridge rgba(255,255,255,.6);
    border-radius: 10px;
    padding: 16px;
    box-shadow: 0 10px 20px rgba(0,0,0,.5);
  }
  .panel h2 {
    font-family: Tahoma, Verdana, sans-serif;
    margin: 0 0 10px;
    font-size: 20px;
    color: #ffffc7;
    text-shadow: 0 0 6px rgba(255,255,255,.5);
  }
  .panel .tag {
    display: inline-block;
    margin: 4px 6px 0 0;
    padding: 4px 8px;
    border-radius: 6px;
    border: 2px solid rgba(255,255,255,.6);
    background: linear-gradient(#00eaff,#0095ff);
    box-shadow: inset 0 1px 0 rgba(255,255,255,.6), 0 2px 6px rgba(0,0,0,.4);
    font-size: 12px; font-weight: 700;
  }

  /* GIF STRIP (placeholders with borders like old "stamps") */
  .gif-strip {
    display: grid; grid-template-columns: repeat(4, 1fr);
    gap: 10px;
  }
  @media (max-width: 720px){ .gif-strip { grid-template-columns: repeat(2, 1fr);} }
  .gif-box {
    border: 2px solid rgba(255,255,255,.7);
    border-radius: 8px;
    background: #000;
    padding: 6px;
    height: 100px;
    display: flex; align-items: center; justify-content: center;
    position: relative; overflow: hidden;
  }
  .gif-box img { max-width: 100%; max-height: 100%; image-rendering: pixelated; }

  /* FOOTER with fake counter */
  footer {
    margin-top: 24px; text-align: center; font-size: 13px;
    opacity: .92;
  }
  .counter {
    display: inline-flex; gap: 2px; align-items: center; padding: 6px 8px;
    background: #00000066; border: 2px inset rgba(255,255,255,.7); border-radius: 6px;
    box-shadow: inset 0 1px 0 rgba(255,255,255,.35), 0 2px 6px rgba(0,0,0,.45);
  }
  .digit {
    width: 16px; height: 22px; display: inline-grid; place-items: center;
    background: linear-gradient(#111, #333); border: 1px solid #999;
    border-radius: 3px; font-family: "Courier New", monospace; font-weight: 700;
  }

  /* Sparkle particles following cursor */
  .sparkle {
    position: fixed; pointer-events: none; width: 10px; height: 10px;
    background: radial-gradient(circle, #fff, rgba(255,255,255,0) 70%);
    filter: drop-shadow(0 0 6px #fff) drop-shadow(0 0 12px #ff66ff);
    will-change: transform, opacity;
  }

  /* Blinking text (emulate old <blink>) */
  .blink { animation: blink 1.2s steps(2, jump-none) infinite; }
  @keyframes blink { 50% { opacity: 0; } }

  /* Minimal "music bar" */
  .player {
    margin-top: 10px;
    background: #0008; padding: 8px; border-radius: 8px; border: 2px solid rgba(255,255,255,.5);
  }

  /* Small helpful hint bubble */
  .hint {
    font-size: 12px; opacity: .85;
  }
</style>
</head>
<body>

<div class="wrap">
  <header class="header">
    <h1 class="nickname">ИНФО САЙТЕКXP</h1>
    <div class="ticker">
      <marquee scrollamount="5" behavior="scroll">&#10024; Добро пожаловать на мой инфо сайт! &#10024; 
        <small>Сделано с крутой крутостью В) • 2007–2010 вайб • Нажми на кнопочки ниже!</small>
      </marquee>
    </div>
    <nav class="nav">
      <a class="btn" href="#about">ОБО МНЕ</a>
      <a class="btn" href="#skills">ЗА ЧТО ШАРЮ</a>
      <a class="btn" href="#gallery">ГИФКИ</a>
      <a class="btn" href="#links">ССЫЛОЧКИ</a>
      <a class="btn" href="#guest">ГОСТЕВАЯ</a>
    </nav>
    <div class="player">
      <b>Музыка:</b> <span class="hint">автовоспроизведение в браузерах блокируют — нажми ▶️</span><br/>
      <audio id="audio" controls>
        <!-- ЗАМЕНИ ССЫЛКУ НИЖЕ НА СВОЙ MP3 -->
        <source src="https://drive.google.com/file/d/10rWY-ui6AKtWEzvH3rrPlUVg4U2J32h0/view?usp=sharing" type="audio/mpeg">
        Твой браузер не поддерживает аудио.
      </audio>
    </div>
  </header>

  <main class="grid">
    <section class="panel" id="about">
      <h2>ОБО МНЕ</h2>
      <p><b>Имя:</b> КРИСТИНА:P</p>
      <p><b>Ник:</b> <span class="blink">SAYONEKA/SAYO</span></p>
      <p><b>О себе:</b> д.р - 13.10, друзей нет, ток племянник:S. Я с Украины, с родного бердянска! Но к сожалению я сейчас в Гайвороне:_(. Ещё я увлекаюсь стилем нулевых, но из этого у меня только штаны клёш, голубая и цветная майка и музыка с тех годов в наушниках. А ну ещё цифровая камера </p>
      <p><b>Дополнительно:</b> Упал - вставай, вставай упай. Упай чокопай </p>
      <p><b>Любимые цвета:</b> бирюзовый • голубой </p>
    </section>

    <section class="panel" id="skills">
      <h2>ЗА ЧТО Я ШАРЮ/ИГРЫ </h2>
      <div>
        <!-- Добавляй/меняй теги ниже -->
        <span class="tag">Roblox</span>
        <span class="tag">Minecraft</span>
        <span class="tag">Colorful Stage</span>
        <span class="tag">Дроны Убийцы</span>
        <span class="tag">Кейон!</span>
        <span class="tag">Уэнсдей</span>
        <span class="tag">Ну крашусь:v</span>

      </div>
      <p style="margin-top:10px;">А у нас, а у нас. А у нас Гуляночкааа!!!</p>
      <ul>
        <li>• льются песни, льются вина</li>
        <li>• и стучат стучат стучат бокалы в такт</li>
        <li>• Ще не вмерла Україна, если мы гуляем так!!!</li>
      </ul>
    </section>

    <section class="panel" id="gallery">
      <h2>МОИ ГИФКИ/БЛЁСТКИ</h2>
      <p class="hint">Вставь свои гифки: нажми правой кнопкой → «Изменить HTML», замени src на ссылки гифок.</p>
      <div class="gif-strip">
        <div class="gif-box"><img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='160' height='100'><rect width='100%' height='100%' fill='black'/><text x='50%' y='52%' dominant-baseline='middle' text-anchor='middle' fill='white' font-family='Verdana' font-size='12'>GIF 2</text></svg>" alt="gif2"/></div>
        <div class="gif-box"><img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='160' height='100'><rect width='100%' height='100%' fill='black'/><text x='50%' y='52%' dominant-baseline='middle' text-anchor='middle' fill='white' font-family='Verdana' font-size='12'>GIF 2</text></svg>" alt="gif2"/></div>
        <div class="gif-box"><img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='160' height='100'><rect width='100%' height='100%' fill='black'/><text x='50%' y='52%' dominant-baseline='middle' text-anchor='middle' fill='white' font-family='Verdana' font-size='12'>GIF 3</text></svg>" alt="gif3"/></div>
        <div class="gif-box"><img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='160' height='100'><rect width='100%' height='100%' fill='black'/><text x='50%' y='52%' dominant-baseline='middle' text-anchor='middle' fill='white' font-family='Verdana' font-size='12'>GIF 4</text></svg>" alt="gif4"/></div>
      </div>
    </section>

    <section class="panel" id="links">
      <h2>ССЫЛОЧКИ</h2>
      <ul>
        <li><a href="https://t.me/SayoNeko0_0" target="_blank">Мой тгк1

        <li><a href="https://t.me/kekmekfek" target="_blank">Мой тгк2
        <li><a href="https://www.roblox.com/users/2205424520/profile" target="_blank">Мой Roblox акк </a></li>
      </ul>
    </section>

    <section class="panel" id="guest">
      <h2>ГОСТЕВАЯ КНИГА</h2>
      <p class="hint">Оставь сообщение себе же (как в старых гостевых) — сохранится в этом браузере.</p>
      <form id="guestForm">
        <input type="text" id="gname" placeholder="Имя/ник" required style="padding:6px; width:48%; max-width:260px; margin-right:6px;">
        <input type="text" id="gtext" placeholder="Сообщение" required style="padding:6px; width:48%; max-width:420px;">
        <button class="btn" type="submit" style="margin-top:6px;">ОТПРАВИТЬ</button>
      </form>
      <div id="guestList" style="margin-top:10px;"></div>
    </section>
  </main>

  <footer>
    <div class="counter" title="С 2008 тут уже побывали:">
      <span style="margin-right:6px;">VISITORS:</span>
      <span class="digit">0</span>
      <span class="digit">0</span>
      <span class="digit">0</span>
      <span class="digit">0</span>
      <span class="digit">1</span>
    </div>
    <div style="margin-top:8px;">© <span id="year"></span> ♥ Юки. Сделано вручную, как в 2008. </div>
  </footer>
</div>

<!-- Cursor sparkle & counters & guestbook -->
<script>
  // Year
  document.getElementById('year').textContent = new Date().getFullYear();

  // Fake "visitor counter" that increments once per browser via localStorage
  (function(){
    const key = "yuki_counter";
    let n = localStorage.getItem(key);
    if(!n){ n = Math.floor(1000 + Math.random()*9000); localStorage.setItem(key, n); } // one-time assign
    const digits = String(n).split('');
    const slots = document.querySelectorAll('.digit');
    // pad left
    while(digits.length < slots.length){ digits.unshift('0'); }
    slots.forEach((el, i)=> el.textContent = digits[digits.length - slots.length + i]);
  })();

  // Guestbook (local only)
  (function(){
    const listKey = "yuki_guestbook";
    const form = document.getElementById('guestForm');
    const list = document.getElementById('guestList');

    function render(){
      const arr = JSON.parse(localStorage.getItem(listKey) || "[]");
      list.innerHTML = arr.map(item => (
        '<div style="margin:6px 0; padding:6px; background:#0006; border:1px solid rgba(255,255,255,.4); border-radius:6px;">' +
        '<b>' + item.name + '</b>: ' + item.text +
        ' <span style="opacity:.7; font-size:12px;">(' + new Date(item.time).toLocaleString() + ')</span>' +
        '</div>'
      )).join('');
    }
    form.addEventListener('submit', e => {
      e.preventDefault();
      const name = document.getElementById('gname').value.trim() || "Anon";
      const text = document.getElementById('gtext').value.trim();
      if(!text) return;
      const arr = JSON.parse(localStorage.getItem(listKey) || "[]");
      arr.unshift({ name, text, time: Date.now() });
      localStorage.setItem(listKey, JSON.stringify(arr));
      form.reset();
      render();
    });
    render();
  })();

  // Cursor sparkles (lightweight)
  (function(){
    const MAX = 40;
    const pool = [];
    function make(x, y){
      const s = document.createElement('div');
      s.className = 'sparkle';
      s.style.left = x + 'px';
      s.style.top = y + 'px';
      s.style.opacity = 1;
      s.vx = (Math.random() - .5) * 1.4;
      s.vy = (Math.random() - 1.8) * 1.2;
      s.life = 600 + Math.random()*400;
      document.body.appendChild(s);
      pool.push({ el: s, born: performance.now() });
      if(pool.length > MAX){
        const old = pool.shift();
        old.el.remove();
      }
    }
    window.addEventListener('mousemove', (e)=>{
      for(let i=0;i<2;i++) make(e.clientX, e.clientY);
    });
    function tick(t){
      for(const p of pool){
        const age = t - p.born;
        const el = p.el;
        const ratio = age / p.el.life;
        if(ratio >= 1){
          el.remove();
          continue;
        }
        const dx = (p.dx || 0) + (Math.random()-.5)*0.2;
        const dy = (p.dy || 0) + 0.6;
        p.dx = dx; p.dy = dy;
        const x = parseFloat(el.style.left) + dx;
        const y = parseFloat(el.style.top) + dy;
        el.style.left = x + 'px';
        el.style.top = y + 'px';
        el.style.opacity = (1 - ratio).toFixed(2);
        el.style.transform = 'scale(' + (1 + ratio*0.8).toFixed(2) + ')';
      }
      requestAnimationFrame(tick);
    }
    requestAnimationFrame(tick);
  })();
</script>

</body>
</html>
