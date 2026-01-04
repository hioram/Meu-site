
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Hioram Martines</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500&family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">
<style>
  * { margin:0; padding:0; box-sizing:border-box; }
  html { scroll-behavior:smooth; }
  body { font-family:'Montserrat', sans-serif; background:#f5f5f3; color:#222; }

  header {
    min-height:100vh;
    background: linear-gradient(rgba(255,255,255,0.8), rgba(255,255,255,0.8)),
                url("fundo.jpg") center/cover no-repeat;
    display:flex; flex-direction:column; justify-content:center; align-items:center;
    text-align:center; padding:40px 20px;
  }
  header img { width:130px; margin-bottom:30px; }
  header h1 { font-family:'Playfair Display', serif; font-size:3rem; letter-spacing:2px; margin-bottom:15px; }
  header p { font-size:1rem; letter-spacing:4px; text-transform:uppercase; color:#777; }

  /* Botão de menu inicial melhorado */
  #botaoMenu {
    position: fixed;
    top:20px;
    right:20px;
    padding:15px 30px;
    font-size:1rem;
    background:#444;
    color:#fff;
    border:none;
    border-radius:8px;
    cursor:pointer;
    font-family:'Playfair Display', serif;
    font-weight:500;
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    transition: 0.3s;
    z-index: 1001;
  }
  #botaoMenu:hover {
    background:#222;
  }

  section { max-width:900px; margin:auto; padding:80px 20px; text-align:center; }
  .impact { font-family:'Playfair Display', serif; font-size:2rem; margin-bottom:60px; cursor:pointer; font-weight:bold; }
  .about { font-size:1.05rem; color:#555; margin-bottom:60px; line-height:1.8; }

  .buttons a { display:inline-block; margin:12px; padding:14px 36px; border:1px solid #222; text-decoration:none; color:#222; font-size:0.9rem; letter-spacing:2px; text-transform:uppercase; transition:0.3s; }
  .buttons a:hover { background:#222; color:#fff; }

  footer { background:#ffffff; padding:40px; text-align:center; font-size:0.8rem; color:#999; position:relative; }

  /* Tela de login */
  #loginScreen {
    position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.8);
    display:none; justify-content:center; align-items:center; z-index:1000;
  }
  #loginBox { background:#fff; padding:40px; border-radius:10px; text-align:center; width:300px; }
  #loginBox input { width:100%; padding:10px; margin:10px 0; border-radius:5px; border:1px solid #ccc; }
  #loginBox button { width:100%; padding:10px; background:#222; color:#fff; border:none; border-radius:5px; cursor:pointer; font-family:'Playfair Display', serif; font-weight:500; }
  #loginBox h2 { margin-bottom:20px; }

  /* Menu lateral */
  #menuLateral {
    position: fixed; top:0; right:-250px; width:250px; height:100%; background:#333; color:#fff;
    transition:0.3s; padding:40px 20px; z-index:1000; display:flex; flex-direction:column;
  }
  #menuLateral button.closeMenu { align-self:flex-end; background:transparent; border:none; color:#fff; font-size:1.5rem; cursor:pointer; }
  #menuLateral a, #menuLateral button.loginMenu { color:#fff; text-decoration:none; margin:15px 0; font-family:'Playfair Display', serif; font-weight:500; background:none; border:none; text-align:left; cursor:pointer; font-size:1rem; }
  #menuLateral a:hover, #menuLateral button.loginMenu:hover { text-decoration:underline; }

  /* Botões de contato finais */
  #contatosFinal div { display:flex; justify-content:center; gap:20px; flex-wrap:wrap; margin-top:40px; }
  #contatosFinal button { padding:15px 30px; font-size:1rem; border:none; border-radius:8px; cursor:pointer; transition:0.3s; color:#fff; background:#222; font-family:'Playfair Display', serif; font-weight:500; }
  #contatosFinal button:hover { background:#555; }
</style>
</head>
<body>

<!-- Tela de login -->
<div id="loginScreen">
  <div id="loginBox">
    <h2>Login</h2>
    <input type="text" id="usuario" placeholder="Usuário">
    <input type="password" id="senha" placeholder="Senha">
    <button onclick="fazerLogin()">Entrar</button>
  </div>
</div>

<!-- Botão de menu -->
<button id="botaoMenu" onclick="abrirMenu()">Menu</button>

<!-- Menu lateral -->
<div id="menuLateral">
  <button class="closeMenu" onclick="fecharMenu()">&times;</button>
  <a href="#contatosFinal" onclick="fecharMenu()">Contato</a>
  <a href="#sobre" onclick="fecharMenu()">Sobre</a>
  <a href="#experiencia" onclick="fecharMenu()">Experiência</a>
  <button class="loginMenu" onclick="abrirLogin()">Login</button>
</div>

<!-- Conteúdo do site -->
<div id="siteContent">
  <header>
    <img src="logo.png" alt="Hioram Martines">
    <h1>HIORAM MARTINES</h1>
    <p>Marca pessoal • Estética • Presença</p>
  </header>

  <section id="sobre">
    <div class="impact" onclick="mudarFrase()">Elegância é quando a presença fala antes das palavras.</div>
    <div class="about">
      Hioram Martines é uma marca pessoal guiada pela estética, pelo cuidado com os detalhes e pela construção de uma identidade sofisticada, limpa e autêntica.
      Cada escolha comunica. Cada presença permanece.
    </div>
  </section>

  <section id="experiencia">
    <h2>Experiência</h2>
    <p class="about">
      Atendimento focado em estética, presença e identidade. Cada detalhe pensado para transmitir sofisticação, cuidado e exclusividade.
    </p>
  </section>

  <!-- Contatos finais com dois botões -->
  <section id="contatosFinal" style="background:#f0f0f0;">
    <h2>Entre em Contato</h2>
    <div>
      <button onclick="abrirWhatsApp1()">WhatsApp</button>
      <button onclick="abrirInstagram()">Instagram</button>
    </div>
  </section>

  <footer>
    © 2026 · Hioram Martines
  </footer>
</div>

<script>
  // Login
  const usuarioCorreto = "hioram";
  const senhaCorreta = "guerra99";

  function abrirLogin() { document.getElementById("loginScreen").style.display="flex"; }

  function fazerLogin(){
    const usuario = document.getElementById("usuario").value.toLowerCase();
    const senha = document.getElementById("senha").value.toLowerCase();
    if(usuario === usuarioCorreto && senha === senhaCorreta){
      document.getElementById("loginScreen").style.display="none";
      alert("Bem-vindo, Hioram!");
    } else {
      alert("Usuário ou senha incorretos!");
      document.getElementById("senha").value="";
    }
  }

  // Menu lateral
  function abrirMenu() { document.getElementById("menuLateral").style.right="0"; }
  function fecharMenu() { document.getElementById("menuLateral").style.right="-250px"; }

  // Botões de contato finais
  function abrirWhatsApp1() { window.open("https://wa.me/message/PIVHCRXKTGIJL1","_blank"); }
  function abrirInstagram() { window.open("https://www.instagram.com/bruno_eu_hioram?igsh=dThsMDFtY2R4Ynp3&utm_source=qr","_blank"); }

  // Frase dinâmica
  function mudarFrase(){
    const frases = [
      "Elegância é quando a presença fala antes das palavras.",
      "Detalhes fazem toda a diferença.",
      "Sofisticação está na autenticidade.",
      "Cada presença comunica mais que palavras."
    ];
    const el = document.querySelector(".impact");
    let nova = frases[Math.floor(Math.random()*frases.length)];
    while(nova===el.textContent){ nova = frases[Math.floor(Math.random()*frases.length)]; }
    el.textContent = nova;
  }
</script>
</body>
</html>
