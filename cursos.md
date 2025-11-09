---
layout: default
title: Cursos e Treinamentos
nav_order: 4
permalink: /cursos/
---
{% include topnav.html %}

# Cursos e Treinamentos

Bem-vindo(a)! Aqui você pode escolher o curso que deseja fazer 👇

<section id="curso-seletor" style="margin-top:20px;">
  <button id="startButton" style="padding:10px 20px;font-size:16px;cursor:pointer;">Ver Cursos</button>

  <div id="opcoes" style="display:none; margin-top:20px;">
    <h3>Escolha seu curso:</h3>
    <button class="curso" data-curso="Python" style="margin-right:10px;">🐍 Python</button>
    <button class="curso" data-curso="R">📊 R</button>
  </div>

  <form id="cadastroForm" style="display:none; margin-top:20px;">
    <h3>Cadastro</h3>
    <label>Email:</label><br>
    <input type="email" id="email" required style="margin-bottom:10px;"><br>
    <label>Número de Matrícula:</label><br>
    <input type="text" id="matricula" required><br><br>
    <button type="submit">Enviar</button>
  </form>

  <p id="mensagem" style="display:none; margin-top:20px; font-weight:bold; color:green;">✅ Cadastro enviado com sucesso!</p>
</section>

<script>
document.getElementById('startButton').addEventListener('click', () => {
  document.getElementById('opcoes').style.display = 'block';
});

document.querySelectorAll('.curso').forEach(button => {
  button.addEventListener('click', () => {
    const curso = button.getAttribute('data-curso');
    localStorage.setItem('cursoEscolhido', curso);
    document.getElementById('cadastroForm').style.display = 'block';
  });
});

document.getElementById('cadastroForm').addEventListener('submit', e => {
  e.preventDefault();
  const email = document.getElementById('email').value;
  const matricula = document.getElementById('matricula').value;
  const curso = localStorage.getItem('cursoEscolhido');

  // Aqui você pode integrar com Google Sheets via Apps Script
  console.log({ email, matricula, curso });

  document.getElementById('cadastroForm').style.display = 'none';
  document.getElementById('mensagem').style.display = 'block';
});
</script>

---

<p class="qe-footer">
  Projeto de Extensão QuantEcon | Universidade Federal de Juiz de Fora — 
  Contato: <a href="mailto:paulo.coimbra@ufjf.br">paulo.coimbra@ufjf.br</a> — Licença MIT
</p>
