---
layout: default
title: Inscrição
nav_order: 4
permalink: /comunidade/inscricao/
---
{% include topnav.html %}

# Inscrição nos Minicursos

{% raw %}
<p>Clique no botão abaixo para escolher seu minicurso e se inscrever:</p>

<button id="btnInscricao" class="btn-primary">Quero me inscrever</button>

<section id="opcoesCurso" style="display:none; margin-top:20px;">
  <p>Escolha o minicurso desejado:</p>
  <button id="btnPython" class="curso-btn">🐍 Python</button>
  <button id="btnR" class="curso-btn">📊 R</button>
</section>

<section id="formulario" style="display:none; margin-top:30px;">
  <h3 id="tituloCurso"></h3>
  <form id="cadastroForm">
    <label>Email institucional:</label><br>
    <input type="email" id="email" required style="margin-bottom:10px; width:250px;"><br>
    <label>Número de matrícula:</label><br>
    <input type="text" id="matricula" required style="margin-bottom:15px; width:200px;"><br>
    <button type="submit" class="btn-enviar">Enviar inscrição</button>
  </form>
  <p id="mensagem" style="display:none; color:green; font-weight:bold; margin-top:10px;">✅ Inscrição enviada com sucesso!</p>
</section>

<style>
.btn-primary {
  background-color: #3e8ed0;
  color: white;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.3s;
}
.btn-primary:hover { background-color: #2b6ca3; }

.curso-btn {
  background-color: #5aa469;
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 8px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 15px;
}
.curso-btn:hover { background-color: #468c54; }

.btn-enviar {
  background-color: #3e8ed0;
  color: white;
  border: none;
  padding: 10px 18px;
  border-radius: 6px;
  cursor: pointer;
}
.btn-enviar:hover { background-color: #2b6ca3; }
</style>

<script>
const btnInscricao = document.getElementById('btnInscricao');
const opcoesCurso = document.getElementById('opcoesCurso');
const formulario = document.getElementById('formulario');
const tituloCurso = document.getElementById('tituloCurso');
const mensagem = document.getElementById('mensagem');

btnInscricao.addEventListener('click', () => {
  opcoesCurso.style.display = 'block';
  btnInscricao.style.display = 'none';
});

function abrirFormulario(curso) {
  tituloCurso.textContent = `Inscrição no Minicurso de ${curso}`;
  formulario.style.display = 'block';
  localStorage.setItem('cursoEscolhido', curso);
}

document.getElementById('btnPython').addEventListener('click', () => abrirFormulario('Python'));
document.getElementById('btnR').addEventListener('click', () => abrirFormulario('R'));

document.getElementById('cadastroForm').addEventListener('submit', e => {
  e.preventDefault();
  const email = document.getElementById('email').value;
  const matricula = document.getElementById('matricula').value;
  const curso = localStorage.getItem('cursoEscolhido');
  console.log("Inscrição recebida:", { email, matricula, curso });
  mensagem.style.display = 'block';
  e.target.reset();
});
</script>
{% endraw %}

---

<script>
const btnInscricao = document.getElementById('btnInscricao');
const opcoesCurso = document.getElementById('opcoesCurso');
const formulario = document.getElementById('formulario');
const tituloCurso = document.getElementById('tituloCurso');
const mensagem = document.getElementById('mensagem');

btnInscricao.addEventListener('click', () => {
  opcoesCurso.style.display = 'block';
  btnInscricao.style.display = 'none';
});

function abrirFormulario(curso) {
  tituloCurso.textContent = `Inscrição no Minicurso de ${curso}`;
  formulario.style.display = 'block';
  localStorage.setItem('cursoEscolhido', curso);
}

document.getElementById('btnPython').addEventListener('click', () => abrirFormulario('Python'));
document.getElementById('btnR').addEventListener('click', () => abrirFormulario('R'));

document.getElementById('cadastroForm').addEventListener('submit', async e => {
  e.preventDefault();
  const email = document.getElementById('email').value;
  const matricula = document.getElementById('matricula').value;
  const curso = localStorage.getItem('cursoEscolhido');

  const data = { email, matricula, curso };

  try {
    const response = await fetch('https://script.google.com/macros/s/AKfycbwwodiL0RbIBPzto50OBs2Crcck7ZCbXeBWjktlQr8KNIfEgcU69--sP_V2xp-lcEDZ/exec', {
      method: 'POST',
      body: JSON.stringify(data),
      headers: { 'Content-Type': 'application/json' }
    });

    // 🟢 Ler e tentar converter a resposta
    const respostaTexto = await response.text();
    console.log("Resposta do servidor:", respostaTexto);

    let resposta;
    try {
      resposta = JSON.parse(respostaTexto);
    } catch {
      resposta = { status: "erro" };
    }

    if (response.ok && resposta.status === "sucesso") {
      mensagem.textContent = "✅ Inscrição enviada com sucesso!";
      mensagem.style.color = "green";
      mensagem.style.display = 'block';
      e.target.reset();
    } else {
      mensagem.textContent = "⚠️ Erro ao enviar inscrição. Tente novamente.";
      mensagem.style.color = "red";
      mensagem.style.display = 'block';
    }

  } catch (error) {
    console.error('Erro ao enviar:', error);
    mensagem.textContent = "❌ Falha de conexão. Tente mais tarde.";
    mensagem.style.color = "red";
    mensagem.style.display = 'block';
  }
});
</script>



