---
layout: default
title: Produtos
nav_order: 20
permalink: /produtos/
---

{% include topnav.html %}

# Produtos Acadêmicos & de Extensão

Explore abaixo todos os produtos produzidos pelo Projeto QuantEcon.  
Use os botões para filtrar por categoria.

<style>
.filter-btn-container {
  margin-bottom: 30px;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}
.filter-btn {
  border: 1px solid #0056b3;
  background-color: white;
  color: #0056b3;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 25px;
  font-weight: 600;
  font-size: 16px;
  transition: all 0.3s ease;
}
.filter-btn:hover, .filter-btn.active {
  background-color: #0056b3;
  color: white;
}
.filter-item { display: none; }
.show { display: block; animation: fadeEffect 0.6s; }
@keyframes fadeEffect {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
.qe-card {
  border: 1px solid #dcdcdc;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 12px;
  background: #fafafa;
}
</style>

<div id="myBtnContainer" class="filter-btn-container">
  <button class="filter-btn active" onclick="filterSelection('all')">Todos</button>
  <button class="filter-btn" onclick="filterSelection('academico')">📚 Acadêmico</button>
  <button class="filter-btn" onclick="filterSelection('ensino')">🎓 Ensino & Eventos</button>
  <button class="filter-btn" onclick="filterSelection('tech')">💾 Dados & Tech</button>
  <button class="filter-btn" onclick="filterSelection('midia')">📢 Mídia & Conteúdo</button>
  <button class="filter-btn" onclick="filterSelection('inst')">🏛️ Institucional</button>
</div>

---

# 📦 Lista de Produtos

<div class="qe-cards">

<!-- ACADÊMICO -->
<div class="qe-card filter-item academico">
  <h3>📚 Monografias & TCCs</h3>
  <a href="/quantecon/docs/produtos/monografias-e-tccs/">Ver mais</a>
</div>

<div class="qe-card filter-item academico">
  <h3>📄 Artigos Científicos</h3>
  <a href="/quantecon/docs/produtos/artigos-cientificos/">Ver mais</a>
</div>

<div class="qe-card filter-item academico">
  <h3>📝 Miniartigos</h3>
  <a href="/quantecon/docs/produtos/miniartigos/">Ver mais</a>
</div>

<!-- ENSINO -->
<div class="qe-card filter-item ensino">
  <h3>🎓 Cursos & Treinamentos</h3>
  <a href="/quantecon/docs/produtos/cursos-e-treinamentos/">Ver mais</a>
</div>

<div class="qe-card filter-item ensino">
  <h3>🚀 Minicursos & Trilhas</h3>
  <a href="/quantecon/docs/produtos/minicuros-e-trilhas/">Ver mais</a>
</div>

<div class="qe-card filter-item ensino">
  <h3>📆 Eventos Promovidos</h3>
  <a href="/quantecon/docs/produtos/eventos-promovidos/">Ver mais</a>
</div>

<div class="qe-card filter-item ensino">
  <h3>🎤 Participações em Eventos</h3>
  <a href="/quantecon/docs/produtos/participacoes-eventos/">Ver mais</a>
</div>

<div class="qe-card filter-item ensino">
  <h3>🧭 Tutoriais</h3>
  <a href="/quantecon/docs/produtos/tutoriais/">Ver mais</a>
</div>

<!-- TECH -->
<div class="qe-card filter-item tech">
  <h3>💾 Códigos & Dados</h3>
  <a href="/quantecon/docs/produtos/codigos-e-dados/">Ver mais</a>
</div>

<div class="qe-card filter-item tech">
  <h3>🛠 Ferramentas & Softwares</h3>
  <a href="/quantecon/docs/produtos/ferramentas-e-softwares/">Ver mais</a>
</div>

<div class="qe-card filter-item tech">
  <h3>📈 Resultados Aplicados</h3>
  <a href="/quantecon/docs/produtos/resultados-aplicados/">Ver mais</a>
</div>

<div class="qe-card filter-item tech">
  <h3>📑 Relatórios Técnicos</h3>
  <a href="/quantecon/docs/produtos/relatorios-tecnicos/">Ver mais</a>
</div>

<!-- MIDIA -->
<div class="qe-card filter-item midia">
  <h3>📊 Boletins</h3>
  <a href="/quantecon/docs/produtos/boletins/">Ver mais</a>
</div>

<div class="qe-card filter-item midia">
  <h3>📰 Newsletter</h3>
  <a href="/quantecon/docs/produtos/newsletter/">Ver mais</a>
</div>

<div class="qe-card filter-item midia">
  <h3>🎬 Vídeos & Webinars</h3>
  <a href="/quantecon/docs/produtos/videos-e-webnars/">Ver mais</a>
</div>

<div class="qe-card filter-item midia">
  <h3>🎧 Podcasts</h3>
  <a href="/quantecon/docs/produtos/podcasts/">Ver mais</a>
</div>

<!-- INSTITUCIONAL -->
<div class="qe-card filter-item inst">
  <h3>🏛 Comunicados</h3>
  <a href="/quantecon/docs/produtos/comunicados/">Ver mais</a>
</div>

<div class="qe-card filter-item inst">
  <h3>📰 Notícias & Divulgação</h3>
  <a href="/quantecon/docs/produtos/noticias-e-divulgacao/">Ver mais</a>
</div>

<div class="qe-card filter-item inst">
  <h3>🤝 Parceiros</h3>
  <a href="/quantecon/docs/produtos/parceiros/">Ver mais</a>
</div>

<div class="qe-card filter-item inst">
  <h3>✨ Outros Produtos</h3>
  <a href="/quantecon/docs/produtos/outros-produtos/">Ver mais</a>
</div>

</div>

<script>
//<![CDATA[
function filterSelection(category) {
  var items = document.getElementsByClassName("filter-item");
  if (category == "all") category = "";

  for (var i = 0; i < items.length; i++) {
    items[i].classList.remove("show");
    if (items[i].className.indexOf(category) > -1) {
      items[i].classList.add("show");
    }
  }
}

document.addEventListener("DOMContentLoaded", function() {
  filterSelection("all");

  var btns = document.querySelectorAll(".filter-btn");
  btns.forEach(btn => {
    btn.addEventListener("click", function() {
      document.querySelector(".filter-btn.active").classList.remove("active");
      this.classList.add("active");
    });
  });
});
//]]>
</script>
