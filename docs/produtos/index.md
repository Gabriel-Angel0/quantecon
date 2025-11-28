---
layout: default
title: Produtos
nav_order: 20
permalink: /produtos/
has_children: true
---

{% include topnav.html %}

<style>
/* Container dos botões */
.filter-btn-container {
  margin-bottom: 30px;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}

/* Botões */
.filter-btn {
  border: 1px solid #0056b3; /* Azul padrão */
  background-color: white;
  color: #0056b3;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 25px;
  font-weight: 600;
  font-size: 16px;
  transition: all 0.3s ease;
  outline: none;
}

/* Estado Hover e Ativo */
.filter-btn:hover, .filter-btn.active {
  background-color: #0056b3;
  color: white;
  text-decoration: none;
}

/* Lógica de Exibição */
.filter-item {
  display: none; /* Esconde tudo por padrão */
}

.show {
  display: block; /* Mostra o que tiver a classe .show */
  animation: fadeEffect 0.6s; /* Efeito suave */
}

/* Animação de entrada */
@keyframes fadeEffect {
  from {opacity: 0; transform: translateY(10px);}
  to {opacity: 1; transform: translateY(0);}
}
</style>


# Produtos Acadêmicos & de Extensão

Explore os produtos acadêmicos & de extensão produzidos pelo projeto. Utilize os botões abaixo para filtrar por categoria:

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
    <p>Trabalhos de conclusão de curso e monografias aprofundando temas específicos em ciência de dados, inteligência artificial, economia e finanças.</p>
    <p><a class="btn" href="{{ '/produtos/monografias-e-tccs/' | relative_url }}">Ver monografias e TCCs</a></p>
  </div>

  <div class="qe-card filter-item academico">
    <h3>📄 Artigos Científicos</h3>
    <p>Produções submetidas a periódicos ou repositórios que apresentam e discutem métodos, técnicas e resultados de pesquisas originais.</p>
    <p><a class="btn" href="{{ '/produtos/artigos-cientificos/' | relative_url }}">Ver artigos científicos</a></p>
  </div>

  <div class="qe-card filter-item academico">
    <h3>📝 Miniartigos</h3>
    <p>Textos curtos que comunicam resultados de análises aplicadas ou estudos de caso de forma objetiva.</p>
    <p><a class="btn" href="{{ '/produtos/miniartigos/' | relative_url }}">Ver miniartigos</a></p>
  </div>

  <div class="qe-card filter-item ensino">
    <h3>🎓 Cursos & Treinamentos</h3>
    <p>Disciplinas completas e programas de formação oferecidos em parceria com departamentos acadêmicos.</p>
    <p><a class="btn" href="{{ '/produtos/cursos-e-treinamentos/' | relative_url }}">Ver cursos & treinamentos</a></p>
  </div>

  <div class="qe-card filter-item ensino">
    <h3>🚀 Minicursos & Trilhas</h3>
    <p>Séries de aulas curtas voltadas para introdução ou atualização rápida em Python, R e IA.</p>
    <p><a class="btn" href="{{ '/produtos/minicuros-e-trilhas/' | relative_url }}">Ver minicursos & trilhas</a></p>
  </div>

  <div class="qe-card filter-item ensino">
    <h3>📆 Eventos Promovidos</h3>
    <p>Workshop, seminários, conferências, jornadas acadêmicas e hackathons organizados pelo projeto.</p>
    <p><a class="btn" href="{{ '/produtos/eventos-promovidos/' | relative_url }}">Ver eventos promovidos</a></p>
  </div>

  <div class="qe-card filter-item ensino">
    <h3>🎤 Participações em Eventos</h3>
    <p>Registros de participação em congressos, seminários, simpósios e painéis acadêmicos.</p>
    <p><a class="btn" href="{{ '/produtos/participacoes-eventos/' | relative_url }}">Ver participações em eventos</a></p>
  </div>

  <div class="qe-card filter-item ensino">
    <h3>🧭 Tutoriais</h3>
    <p>Guias passo a passo com código e dados para replicação de análises e implementação de algoritmos.</p>
    <p><a class="btn" href="{{ '/produtos/tutoriais/' | relative_url }}">Ver tutoriais</a></p>
  </div>

  <div class="qe-card filter-item tech">
    <h3>💾 Códigos & Dados</h3>
    <p>Repositórios de notebooks, pacotes de código, APIs, datasets abertos e coleções de dados.</p>
    <p><a class="btn" href="{{ '/produtos/codigos-e-dados/' | relative_url }}">Ver códigos & dados</a></p>
  </div>

  <div class="qe-card filter-item tech">
    <h3>🛠️ Ferramentas & Softwares</h3>
    <p>Pacotes de software, bibliotecas, scripts reutilizáveis e aplicações web desenvolvidos pelo projeto.</p>
    <p><a class="btn" href="{{ '/produtos/ferramentas-e-softwares/' | relative_url }}">Ver ferramentas & softwares</a></p>
  </div>

  <div class="qe-card filter-item tech">
    <h3>📈 Resultados Aplicados</h3>
    <p>Comparações entre modelos, cenários de simulação e análises estatísticas realizadas no âmbito do projeto.</p>
    <p><a class="btn" href="{{ '/produtos/resulktados-aplicados/' | relative_url }}">Ver resultados aplicados</a></p>
  </div>

  <div class="qe-card filter-item tech">
    <h3>📑 Relatórios Técnicos & Painéis</h3>
    <p>Documentos sobre metodologias e resultados, além de painéis de indicadores e dashboards interativos.</p>
    <p><a class="btn" href="{{ '/produtos/relatorios-tecnicos/' | relative_url }}">Ver relatórios técnicos</a></p>
  </div>

  <div class="qe-card filter-item midia">
    <h3>📊 Boletins</h3>
    <p>Publicações periódicas com análises econômicas, financeiras e tecnológicas.</p>
    <p><a class="btn" href="{{ '/produtos/boletins/' | relative_url }}">Ver boletins</a></p>
  </div>

  <div class="qe-card filter-item midia">
    <h3>📰 Newsletter</h3>
    <p>Fique por dentro das principais análises e novidades com a nossa newsletter periódica.</p>
    <p><a class="btn" href="{{ '/produtos/newsletter/' | relative_url }}">Ver newsletter</a></p>
  </div>

  <div class="qe-card filter-item midia">
    <h3>🎬 Vídeos & Webinars</h3>
    <p>Playlists de aulas, apresentações, webinars ao vivo e gravações de palestras.</p>
    <p><a class="btn" href="{{ '/produtos/videos-e-webnars/' | relative_url }}">Ver videos & webinars</a></p>
  </div>

  <div class="qe-card filter-item midia">
    <h3>🎧 Podcasts</h3>
    <p>Programas de áudio disponibilizados online sob demanda sobre ciência de dados e economia.</p>
    <p><a class="btn" href="{{ '/produtos/podcasts/' | relative_url }}">Ver podcasts</a></p>
  </div>

  <div class="qe-card filter-item inst">
    <h3>📢 Comunicados</h3>
    <p>Anúncios oficiais sobre parcerias, próximos eventos e chamadas públicas.</p>
    <p><a class="btn" href="{{ '/produtos/comunicados/' | relative_url }}">Ver comunicados</a></p>
  </div>

  <div class="qe-card filter-item inst">
    <h3>📰 Notícias & Divulgações</h3>
    <p>Notas sobre eventos, conquistas do projeto e oportunidades de colaboração.</p>
    <p><a class="btn" href="{{ '/produtos/noticias-e-divulgacao/' | relative_url }}">Ver notícias & divulgações</a></p>
  </div>

  <div class="qe-card filter-item inst">
    <h3>✨ Outros Produtos</h3>
    <p>Seção dedicada a estudos de caso e outras iniciativas inovadoras.</p>
    <p><a class="btn" href="{{ '/produtos/outros-produtos/' | relative_url }}">Ver outros produtos</a></p>
  </div>

</div>

---

<p class="qe-footer">
  Projeto de Extensão QuantEcon | Universidade Federal de Juiz de Fora — 
  Contato: <a href="mailto:paulo.coimbra@ufjf.br">paulo.coimbra@ufjf.br</a> — Licença MIT
</p>

<script type="text/javascript">
  // CORREÇÃO: Usamos 'window.' para garantir que as funções sejam globais
  // e acessíveis pelos botões, evitando o ReferenceError.

  window.filterSelection = function(c) {
    var x, i;
    x = document.getElementsByClassName("filter-item");
    if (c == "all") c = "";
    for (i = 0; i < x.length; i++) {
      w3RemoveClass(x[i], "show");
      if (x[i].className.indexOf(c) > -1) w3AddClass(x[i], "show");
    }
  }

  window.w3AddClass = function(element, name) {
    var i, arr1, arr2;
    arr1 = element.className.split(" ");
    arr2 = name.split(" ");
    for (i = 0; i < arr2.length; i++) {
      if (arr1.indexOf(arr2[i]) == -1) {element.className += " " + arr2[i];}
    }
  }

  window.w3RemoveClass = function(element, name) {
    var i, arr1, arr2;
    arr1 = element.className.split(" ");
    arr2 = name.split(" ");
    for (i = 0; i < arr2.length; i++) {
      while (arr1.indexOf(arr2[i]) > -1) {
        arr1.splice(arr1.indexOf(arr2[i]), 1);     
      }
    }
    element.className = arr1.join(" ");
  }

  // Inicialização segura após o carregamento da página
  document.addEventListener("DOMContentLoaded", function() {
    // Mostra todos inicialmente
    filterSelection("all");

    // Adiciona lógica de botão ativo
    var btnContainer = document.getElementById("myBtnContainer");
    if(btnContainer){
        var btns = btnContainer.getElementsByClassName("filter-btn");
        for (var i = 0; i < btns.length; i++) {
          btns[i].addEventListener("click", function(){
            var current = document.getElementsByClassName("active");
            if(current.length > 0){
                current[0].className = current[0].className.replace(" active", "");
            }
            this.className += " active";
          });
        }
    }
  });
</script>
