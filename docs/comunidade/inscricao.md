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
---
layout: default
title: Inscrição
nav_order: 4
permalink: /comunidade/inscricao/
---
{% include topnav.html %}

# Inscrição nos Minicursos

<iframe 
  src="<iframe src="<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSc8RBwk8BPDlu3zvH3qiy1vEC1SQWSm3S2UThp2M_pnBvYk9g/viewform?embedded=true" width="640" height="863" frameborder="0" marginheight="0" marginwidth="0">Carregando…</iframe>"
  width="640" 
  height="800" 
  frameborder="0" 
  marginheight="0" 
  marginwidth="0">
  Carregando…
</iframe>

<p class="qe-footer">
  Projeto de Extensão QuantEcon | Universidade Federal de Juiz de Fora — 
  Contato: <a href="mailto:paulo.coimbra@ufjf.br">paulo.coimbra@ufjf.br</a> — Licença MIT
</p>

</script>
{% endraw %}

---

<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Inscrição Minicurso</title>
</head>
<body>
  <h1>Inscreva-se para o Minicurso</h1>

  <iframe 
    src="<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSc8RBwk8BPDlu3zvH3qiy1vEC1SQWSm3S2UThp2M_pnBvYk9g/viewform?embedded=true" width="640" height="863" frameborder="0" marginheight="0" marginwidth="0">Carregando…</iframe>"
    width="640"
    height="800"
    frameborder="0"
    marginheight="0"
    marginwidth="0">
    Carregando…
  </iframe>
</body>
</html>



