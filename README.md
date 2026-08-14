<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AULA DIGITAL - Algoritmos y Redes Sociales</title>

<style>
:root{
    --bg:#070913;
    --card:#0f1322;
    --card2:#090d1a;
    --border:#1f2740;
    --cyan:#00f2fe;
    --pink:#ff0050;
    --purple:#8a2be2;
    --green:#00e676;
    --yellow:#ffd600;
    --text:#f0f2f8;
    --dim:#94a3b8;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Arial,sans-serif;
}

html{
    scroll-behavior:smooth;
}

body{
    background:
        radial-gradient(circle at top right,rgba(138,43,226,.12),transparent 30%),
        radial-gradient(circle at top left,rgba(0,242,254,.08),transparent 25%),
        var(--bg);
    color:var(--text);
    padding:20px 12px;
    line-height:1.6;
}

.container{
    max-width:850px;
    margin:auto;
}

.top-bar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    margin-bottom:22px;
    padding-bottom:15px;
    border-bottom:1px solid var(--border);
    position:relative;
}

.brand-wrapper{
    display:flex;
    align-items:center;
    gap:12px;
}

.menu-toggle{
    background:#14192e;
    border:1px solid var(--border);
    color:var(--cyan);
    font-size:20px;
    padding:6px 12px;
    border-radius:8px;
    cursor:pointer;
}

.brand{
    font-size:20px;
    font-weight:900;
    letter-spacing:1.5px;
    cursor:pointer;
}

.brand span{
    color:var(--pink);
}

.badge{
    background:rgba(0,242,254,.1);
    border:1px solid var(--cyan);
    color:var(--cyan);
    padding:4px 10px;
    border-radius:20px;
    font-size:11px;
    font-weight:700;
}

.dropdown-menu{
    display:none;
    position:absolute;
    top:55px;
    left:0;
    width:285px;
    background:var(--card);
    border:1px solid var(--cyan);
    border-radius:12px;
    box-shadow:0 10px 30px rgba(0,242,254,.2);
    z-index:1000;
    overflow:hidden;
}

.dropdown-menu.active{
    display:block;
}

.dropdown-item{
    display:block;
    padding:14px 16px;
    color:var(--text);
    text-decoration:none;
    font-size:14px;
    font-weight:700;
    border-bottom:1px solid var(--border);
    cursor:pointer;
}

.dropdown-item:hover{
    background:rgba(0,242,254,.1);
    color:var(--cyan);
}

.view-section{
    display:none;
}

.view-section.active-view{
    display:block;
}

.intro-hero{
    background:linear-gradient(135deg,#0f1322,#14192e);
    border:1px solid var(--border);
    border-left:5px solid var(--cyan);
    border-radius:16px;
    padding:24px;
    margin-bottom:28px;
    box-shadow:0 10px 30px rgba(0,0,0,.4);
}

.intro-hero h1{
    font-size:27px;
    margin-bottom:8px;
}

.intro-hero p{
    color:var(--dim);
    margin-bottom:18px;
}

.section-tag{
    color:var(--cyan);
    font-size:12px;
    font-weight:900;
    text-transform:uppercase;
    letter-spacing:1.5px;
    margin-bottom:8px;
}

.team-box{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
    gap:12px;
    background:var(--card2);
    border:1px solid var(--border);
    padding:14px;
    border-radius:12px;
}

.team-item{
    font-size:13px;
}

.team-item strong{
    color:var(--cyan);
    display:block;
    font-size:11px;
    text-transform:uppercase;
}

.card{
    background:var(--card);
    border:1px solid var(--border);
    border-radius:16px;
    padding:24px;
    margin-bottom:24px;
    box-shadow:0 10px 30px rgba(0,0,0,.4);
}

.card h2{
    font-size:20px;
    margin-bottom:10px;
}

.card p{
    color:var(--dim);
    font-size:15px;
    margin-bottom:15px;
}

.video-wrapper{
    position:relative;
    padding-bottom:56.25%;
    height:0;
    overflow:hidden;
    border-radius:12px;
    border:2px solid var(--cyan);
    background:#000;
}

.video-wrapper iframe{
    position:absolute;
    inset:0;
    width:100%;
    height:100%;
    border:0;
}

.btn{
    display:block;
    width:100%;
    border:none;
    border-radius:10px;
    padding:13px;
    font-weight:900;
    cursor:pointer;
}

.btn-cyan{
    background:var(--cyan);
    color:#000;
}

.btn-green{
    background:var(--green);
    color:#000;
}

.back-btn{
    background:#14192e;
    border:1px solid var(--border);
    color:var(--cyan);
    padding:8px 16px;
    border-radius:8px;
    font-weight:800;
    cursor:pointer;
    margin-bottom:20px;
}

.input{
    width:100%;
    padding:14px;
    border-radius:10px;
    border:1px solid var(--border);
    background:var(--card2);
    color:#fff;
    outline:none;
    font-size:16px;
    margin-bottom:12px;
}

.input:focus{
    border-color:var(--cyan);
}

.hours-display{
    text-align:center;
    font-size:38px;
    font-weight:900;
    color:var(--cyan);
    margin:12px 0;
}

.slider{
    width:100%;
    accent-color:var(--cyan);
    cursor:pointer;
}

.calc-box{
    background:#05070f;
    border-left:4px solid var(--pink);
    padding:15px;
    border-radius:8px;
    margin-top:15px;
}

.opt-btn{
    display:block;
    width:100%;
    text-align:left;
    background:#14192e;
    border:1px solid var(--border);
    color:var(--text);
    padding:14px;
    border-radius:10px;
    font-size:14px;
    margin-bottom:10px;
    cursor:pointer;
}

.opt-btn:hover{
    border-color:var(--cyan);
}

.opt-btn.correct{
    background:rgba(0,230,118,.15)!important;
    border-color:var(--green)!important;
}

.opt-btn.incorrect{
    background:rgba(255,0,80,.15)!important;
    border-color:var(--pink)!important;
}

.feedback{
    display:none;
    padding:12px;
    border-radius:10px;
    margin-top:8px;
    font-size:14px;
}

.score-banner{
    background:linear-gradient(135deg,#14192e,#090d1a);
    border:1px solid var(--cyan);
    border-radius:12px;
    padding:15px;
    margin-bottom:20px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.score-counter{
    font-weight:900;
    font-size:16px;
    color:var(--cyan);
}

.tabs{
    display:flex;
    gap:8px;
    flex-wrap:wrap;
}

.tab{
    flex:1;
    min-width:100px;
    padding:11px;
    border-radius:10px;
    background:#14192e;
    color:var(--dim);
    border:1px solid var(--border);
    cursor:pointer;
    font-weight:800;
}

.tab.active{
    background:var(--cyan);
    color:#000;
}

.tab-info{
    margin-top:12px;
    background:var(--card2);
    border:1px solid var(--border);
    border-radius:12px;
    padding:16px;
    color:var(--dim);
}

textarea{
    width:100%;
    height:90px;
    resize:none;
    background:var(--card2);
    border:1px solid var(--border);
    border-radius:10px;
    color:#fff;
    padding:12px;
    outline:none;
}

.status{
    display:none;
    margin-top:12px;
    padding:12px;
    border-radius:10px;
    text-align:center;
    font-weight:700;
}

footer{
    text-align:center;
    padding:30px 10px;
    border-top:1px solid var(--border);
    margin-top:40px;
    color:var(--dim);
}

@media(max-width:600px){
    .badge{display:none;}
}
</style>
</head>

<body>

<div class="container">

<div class="top-bar">
    <div class="brand-wrapper">
        <button class="menu-toggle" onclick="toggleMenu()">&#9776;</button>
        <div class="brand" onclick="switchView('home')">
            AULA DIGITAL <span>&#8226;</span>
        </div>
    </div>

    <div class="badge">Unidad Did&aacute;ctica Interactiva</div>

    <div class="dropdown-menu" id="menu">
        <div class="dropdown-item" onclick="switchView('home')">&#127968; Inicio</div>
        <div class="dropdown-item" onclick="switchView('sim')">&#128241; Simulador de tel&eacute;fono</div>
        <div class="dropdown-item" onclick="switchView('act')">&#128736; Actividades</div>
        <div class="dropdown-item" onclick="switchView('ref')">&#128173; Reflexi&oacute;n</div>
    </div>
</div>


<!-- ================= INICIO ================= -->

<section id="home" class="view-section active-view">

<div class="intro-hero">

<div class="section-tag">PORTADA EDITORIAL</div>

<h1>Ciudadan&iacute;a Digital y Redes Sociales</h1>

<p>
&iquest;Por qu&eacute; TikTok parece saber exactamente qu&eacute; queremos mirar?
En esta unidad vamos a descubrir c&oacute;mo funcionan los algoritmos de recomendaci&oacute;n,
la inteligencia artificial y la llamada "burbuja de filtro".
</p>

<div class="team-box">

<div class="team-item">
<strong>Materia</strong>
Tecnolog&iacute;a de la Informaci&oacute;n y la Comunicaci&oacute;n
</div>

<div class="team-item">
<strong>Curso</strong>
4.&ordm; A&ntilde;o
</div>

<div class="team-item">
<strong>Integrantes</strong>
Santiago Vilches &middot; Lautaro Gutierrez
</div>

</div>

</div>

<div class="section-tag">RECURSO AUDIOVISUAL</div>

<div class="card">

<h2>&#128249; Algoritmos de TikTok</h2>

<p>
Mir&aacute; el video y despu&eacute;s realiz&aacute; las actividades.
</p>

<div class="video-wrapper">
<iframe
src="https://www.youtube.com/embed/nOFEjAHZ8ig"
title="Algoritmos de TikTok"
allowfullscreen>
</iframe>
</div>

</div>

<div class="card">

<h2>&#127919; &iquest;Qu&eacute; vamos a investigar?</h2>

<p>
Vamos a analizar cu&aacute;nto tiempo pasamos con el tel&eacute;fono,
qu&eacute; se&ntilde;ales utilizamos en las redes sociales y c&oacute;mo esas acciones
pueden modificar el contenido que aparece en nuestro feed.
</p>

<button class="btn btn-cyan" onclick="switchView('sim')">
&#128241; Comenzar simulador
</button>

</div>

</section>


<!-- ================= SIMULADOR ================= -->

<section id="sim" class="view-section">

<button class="back-btn" onclick="switchView('home')">
&larr; Volver al inicio
</button>

<div class="section-tag">01 &bull; DATOS DE LA CLASE</div>

<h1>&#128241; &iquest;Cu&aacute;ntas horas pas&aacute;s con el tel&eacute;fono?</h1>

<div class="card">

<h2>Simulador de uso del tel&eacute;fono</h2>

<p>
Mov&eacute; el control para indicar aproximadamente cu&aacute;ntas horas por d&iacute;a
pas&aacute;s usando el tel&eacute;fono.
</p>

<div class="hours-display">
<span id="hoursValue">5</span> h/d&iacute;a
</div>

<input
type="range"
id="hoursSlider"
class="slider"
min="0.5"
max="15"
step="0.5"
value="5"
oninput="updateHours()">

<div class="calc-box" id="calcResult"></div>

</div>

<div class="card">

<h2>&#128100; Datos del Alumno</h2>

<p>
Ingres&aacute; tu Nombre y Apellido para poder mandar los resultados al profesor.
</p>

<input
class="input"
id="studentName"
maxlength="40"
placeholder="Tu Nombre y Apellido (Obligatorio)">

<button class="btn btn-green" onclick="switchView('act')">
Ir a responder las actividades &rarr;
</button>

</div>

</section>


<!-- ================= ACTIVIDADES ================= -->

<section id="act" class="view-section">

<button class="back-btn" onclick="switchView('home')">
&larr; Volver al inicio
</button>

<div class="section-tag">02 &bull; LABORATORIO</div>

<h1>&#128736; Actividades</h1>

<!-- Marcador de Puntaje Vivo -->
<div class="score-banner">
    <div>Tu progreso en vivo:</div>
    <div class="score-counter">
        <span style="color:var(--green)">&#9989; <span id="correctCount">0</span></span> | 
        <span style="color:var(--pink)">&#10060; <span id="incorrectCount">0</span></span> 
        / 7 Respondidas
    </div>
</div>


<div class="card">

<h2>1&#65039;&#8419; Se&ntilde;ales del algoritmo</h2>

<p>
&iquest;Cu&aacute;l de estas acciones puede darle una se&ntilde;al fuerte al algoritmo
para mostrarte contenido similar?
</p>

<button class="opt-btn"
onclick="answer(this,true,'f1','Mirar un video durante mucho tiempo es una se\u00f1al muy importante para los sistemas de recomendaci\u00f3n.')">
A) Mirar el video completo o dejar que se repita.
</button>

<button class="opt-btn"
onclick="answer(this,false,'f1','El me gusta es una se\u00f1al, pero no es la \u00fanica. El tiempo de visualizaci\u00f3n es m&aacute;s determinante.')">
B) Dar un me gusta r&aacute;pido y pasar inmediatamente.
</button>

<div id="f1" class="feedback"></div>

</div>


<div class="card">

<h2>2&#65039;&#8419; Comparativo de plataformas</h2>

<div class="tabs">

<button class="tab active" onclick="tab('tt',this)">
TikTok
</button>

<button class="tab" onclick="tab('ig',this)">
Instagram
</button>

<button class="tab" onclick="tab('yt',this)">
YouTube
</button>

</div>

<div class="tab-info" id="tabInfo">
<strong style="color:var(--cyan)">TikTok:</strong>
analiza numerosas se&ntilde;ales de interacci&oacute;n para personalizar el contenido.
</div>

</div>


<div class="card">

<h2>3&#65039;&#8419; Fake News</h2>

<p>
Un video tiene millones de likes y afirma que una bebida cura enfermedades.
&iquest;Qu&eacute; hac&eacute;s?
</p>

<button class="opt-btn"
onclick="answer(this,true,'f3','\u00a1Excelente! La cantidad de likes no demuestra que una informaci\u00f3n sea verdadera. Hay que verificar fuentes.')">
A) Verificar la informaci&oacute;n en fuentes confiables.
</button>

<button class="opt-btn"
onclick="answer(this,false,'f3','Incorrecto. Que algo sea viral no significa que sea seguro ni verdadero.')">
B) Compartirlo porque tiene millones de likes.
</button>

<div id="f3" class="feedback"></div>

</div>


<div class="card">

<h2>4&#65039;&#8419; C&aacute;mara de eco</h2>

<p>
&iquest;Con qu&eacute; frecuencia encontr&aacute;s opiniones diferentes a las tuyas en tu feed?
</p>

<button class="opt-btn"
onclick="answer(this,false,'f4','Ver siempre opiniones iguales puede limitar la diversidad de informaci\u00f3n que recib&iacute;s.')">
A) Casi nunca.
</button>

<button class="opt-btn"
onclick="answer(this,true,'f4','Muy bien. Encontrar puntos de vista diferentes ayuda a desarrollar el pensamiento cr\u00edtico.')">
B) Frecuentemente.
</button>

<div id="f4" class="feedback"></div>

</div>


<div class="card">

<h2>5&#65039;&#8419; Privacidad</h2>

<p>
&iquest;Qu&eacute; puede ocurrir cuando una aplicaci&oacute;n obtiene muchos datos sobre nuestros h&aacute;bitos?
</p>

<button class="opt-btn"
onclick="answer(this,true,'f5','Correcto. Los datos se usan para construir perfiles y personalizar contenidos y publicidad.')">
A) Puede construir un perfil preciso de nuestros intereses.
</button>

<button class="opt-btn"
onclick="answer(this,false,'f5','No. Los datos sirven para personalizar completamente lo que ves en pantalla.')">
B) Solo sirven para evitar errores de la aplicaci&oacute;n.
</button>

<div id="f5" class="feedback"></div>

</div>


<div class="card">

<h2>6&#65039;&#8419; Scroll infinito</h2>

<p>
&iquest;Por qu&eacute; seguimos deslizando aunque no sepamos qu&eacute; video aparecer&aacute; despu&eacute;s?
</p>

<button class="opt-btn"
onclick="answer(this,true,'f6','Correcto. La incertidumbre sobre cu\u00e1l ser\u00e1 el pr&oacute;ximo contenido estimula a seguir explorando.')">
A) Porque buscamos la pr&oacute;xima recompensa o contenido interesante.
</button>

<button class="opt-btn"
onclick="answer(this,false,'f6','El scroll infinito est\u00e1 dise\u00f1ado para incentivar el consumo continuo.')">
B) Porque es un error de dise&ntilde;o de la aplicaci&oacute;n.
</button>

<div id="f6" class="feedback"></div>

</div>


<div class="card">

<h2>7&#65039;&#8419; Contenido pol&eacute;mico</h2>

<p>
&iquest;Qu&eacute; puede ocurrir cuando una publicaci&oacute;n genera muchos comentarios e interacciones agresivas?
</p>

<button class="opt-btn"
onclick="answer(this,true,'f7','Correcto. La pol\u00e9mica genera interacciones que el algoritmo puede interpretar como relevancia.')">
A) El sistema suele darle mayor difusi&oacute;n por la cantidad de comentarios.
</button>

<button class="opt-btn"
onclick="answer(this,false,'f7','No necesariamente. La pol\u00e9mica suele retener la atenci&oacute;n del usuario.')">
B) Siempre desaparece de forma autom&aacute;tica.
</button>

<div id="f7" class="feedback"></div>

</div>


<div class="card">

<h2>8&#65039;&#8419; Compromiso personal</h2>

<p>
Escrib&iacute; una acci&oacute;n que podr&iacute;as realizar para controlar mejor tu consumo digital.
</p>

<textarea
id="commitment"
placeholder="Ejemplo: voy a limitar mi tiempo de TikTok...">
</textarea>

</div>


<!-- Cartel Final para Enviar Datos -->
<div class="card" id="finalQuizResult" style="border: 2px solid var(--cyan);">

<h2>&#128221; Guardar en la Planilla del Profesor</h2>

<p id="quizSummaryText">
Al tocar el bot&oacute;n de abajo, tus datos y tus calificaciones se guardar&aacute;n autom&aacute;ticamente en la planilla de Google Sheets.
</p>

<button id="btnSendMail" class="btn btn-green" onclick="sendToTeacher()">
&#128640; Enviar resultados a la Planilla
</button>

<div id="sendStatus" class="status"></div>

</div>

</section>


<!-- ================= REFLEXIÓN ================= -->

<section id="ref" class="view-section">

<button class="back-btn" onclick="switchView('home')">
&larr; Volver al inicio
</button>

<div class="section-tag">03 &bull; REFLEXI&Oacute;N</div>

<h1>&#128173; Para pensar</h1>

<div class="card">

<h2>&iquest;Tu feed representa todo Internet?</h2>

<p>
No. El feed es solamente una selecci&oacute;n de contenido determinada
por diferentes se&ntilde;ales, intereses e interacciones.
</p>

</div>

<div class="card">

<h2>&#127919; Conclusi&oacute;n</h2>

<p style="color:#fff;font-size:17px">
El algoritmo aprende de nuestras acciones, pero nosotros podemos
aprender a cuestionar lo que el algoritmo nos muestra.
</p>

</div>

</section>


<footer>

<strong>AULA DIGITAL &bull; Ciudadan&iacute;a Digital y Redes Sociales &bull; 4.&ordm; A&ntilde;o</strong>

<p>Santiago Vilches &middot; Lautaro Gutierrez</p>

</footer>

</div>


<script>

let correctAnswers = 0;
let incorrectAnswers = 0;

function toggleMenu(){
    document.getElementById("menu").classList.toggle("active");
}

function switchView(id){
    document.querySelectorAll(".view-section").forEach(v => v.classList.remove("active-view"));
    document.getElementById(id).classList.add("active-view");
    document.getElementById("menu").classList.remove("active");
    window.scrollTo({top:0, behavior:"smooth"});
}

function updateHours(){
    const hours = Number(document.getElementById("hoursSlider").value);
    document.getElementById("hoursValue").innerText = hours;
    const weekly = (hours * 7).toFixed(1);
    const days = ((hours * 365) / 24).toFixed(1);

    document.getElementById("calcResult").innerHTML =
    "En una semana ser\u00edan aprox. <strong>" + weekly + " hs</strong>. Al a\u00f1o equivale a <strong>" + days + " d\u00edas enteros</strong> usando el celular.";
}

function answer(btn, isCorrect, feedbackId, text){
    const container = btn.parentElement;
    const buttons = container.querySelectorAll('.opt-btn');
    
    buttons.forEach(b => {
        b.disabled = true;
        b.style.cursor = "default";
        b.style.opacity = "0.7";
    });

    if(isCorrect){
        btn.classList.add("correct");
        correctAnswers++;
        document.getElementById("correctCount").innerText = correctAnswers;
    } else {
        btn.classList.add("incorrect");
        incorrectAnswers++;
        document.getElementById("incorrectCount").innerText = incorrectAnswers;
    }

    const fb = document.getElementById(feedbackId);
    fb.style.display = "block";
    fb.style.background = isCorrect ? "rgba(0,230,118,0.15)" : "rgba(255,0,80,0.15)";
    fb.style.color = isCorrect ? "var(--green)" : "var(--pink)";
    fb.innerText = text;
}

function tab(platform, btn){
    document.querySelectorAll(".tab").forEach(t => t.classList.remove("active"));
    btn.classList.add("active");
    const info = document.getElementById("tabInfo");
    if(platform === 'tt'){
        info.innerHTML = "<strong style='color:var(--cyan)'>TikTok:</strong> analiza tiempo de permanencia, reproducciones seguidas y compartidos.";
    } else if(platform === 'ig'){
        info.innerHTML = "<strong style='color:var(--cyan)'>Instagram:</strong> prioriza interacciones con amigos cercanos, guardados y mensajes directos.";
    } else if(platform === 'yt'){
        info.innerHTML = "<strong style='color:var(--cyan)'>YouTube:</strong> se enfoca en el historial de b\u00fasqueda, duraci\u00f3n del video y tasa de clics.";
    }
}

async function sendToTeacher(){
    const name = document.getElementById("studentName").value.trim();
    const hours = document.getElementById("hoursValue").innerText;
    const commitment = document.getElementById("commitment").value.trim();
    const status = document.getElementById("sendStatus");
    const btn = document.getElementById("btnSendMail");

    if(!name){
        alert("Por favor, ingres\u00e1 tu Nombre y Apellido en el Simulador antes de enviar.");
        switchView('sim');
        return;
    }

    status.style.display = "block";
    status.style.background = "rgba(0,242,254,0.15)";
    status.style.color = "var(--cyan)";
    status.innerText = "Guardando respuestas en la planilla...";
    btn.disabled = true;

    // Tu nueva URL desplegada:
    const baseUrl = "https://script.google.com/macros/s/AKfycbyrsNuVAC7aJlq2M9RAhpv9q7Sp7FLQeX_rbp2t_XjLSfGZaaKgC64Nx791VBnl4Wev/exec";

    const params = new URLSearchParams({
        "Alumno": name,
        "Horas": hours + " hs/d\u00eda",
        "Correctas": correctAnswers,
        "Incorrectas": incorrectAnswers,
        "Compromiso": commitment || "Sin respuesta"
    });

    try {
        await fetch(`${baseUrl}?${params.toString()}`, {
            method: "GET",
            mode: "no-cors"
        });

        status.style.background = "rgba(0,230,118,0.2)";
        status.style.color = "var(--green)";
        status.innerText = "\u2705 \u00a1Tus respuestas se guardaron correctamente en la planilla!";
    } catch (error) {
        status.style.background = "rgba(255,0,80,0.2)";
        status.style.color = "var(--pink)";
        status.innerText = "\u274c Hubo un error al guardar. Intent\u00e1 de nuevo.";
        btn.disabled = false;
    }
}

updateHours();

</script>

</body>
</html>
