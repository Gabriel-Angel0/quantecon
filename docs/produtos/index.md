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
</style>

<div id="myBtnContainer" class="filter-btn-container">
  <button class="filter-btn active" onclick="filterSelection('all')">Todos</button>
  <button class="filter-btn" onclick="filterSelection('academico')">📚 Acadêmico</button>
  <button class="filter-btn" onclick="filterSelection('ensino')">🎓 Ensino & Eventos</button>
  <button class="filter-btn" onclick="filterSelection('tech')">💾 Dados & Tech</button>
  <button class="filter-btn" onclick="filterSelection('midia')">📢 Mídia & Conteúdo</button>
  <button class="filter-btn" onclick="filterSelection('inst')">🏛️ Institucional</button>
</div>

<div class="qe-cards">

  <div class="qe-card filter-item academico">
    <h3>📚 Monografias & TCCs</h3>
    <p><a class="btn" href="/produtos/monografias-e-tccs/">Ver monografias e TCCs</a></p>
  </div>

  <div class="qe-card filter-item academico">
    <h3>📄 Artigos Científicos</h3>
    <p><a class="btn" href="/produtos/artigos-cientificos/">Ver artigos científicos</a></p>
  </div>

  <div class="qe-card filter-item ensino">
    <h3>🎓 Cursos & Treinamentos</h3>
    <p><a class="btn" href="/produtos/cursos-e-treinamentos/">Ver cursos & treinamentos</a></p>
  </div>

  <div class="qe-card filter-item tech">
    <h3>💾 Códigos & Dados</h3>
    <p><a class="btn" href="/produtos/codigos-e-dados/">Ver códigos & dados</a></p>
  </div>

  <div class="qe-card filter-item midia">
    <h3>📊 Boletins</h3>
    <p><a class="btn" href="/produtos/boletins/">Ver boletins</a></p>
  </div>

  <div class="qe-card filter-item inst">
    <h3>📢 Comunicados</h3>
    <p><a class="btn" href="/produtos/comunicados/">Ver comunicados</a></p>
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
