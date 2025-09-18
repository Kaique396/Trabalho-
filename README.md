# Trabalho-
document.addEventListener('DOMContentLoaded', function () {  
    const botaoDeAcessibilidade = document.getElementById('botao-acessibilidade')
    const opcoesDeAcessibilidade = document.getElementById('opcoes-acessibilidade')

    botaoDeAcessibilidade.addEventListener('click', function () {
        botaoDeAcessibilidade.classList.toggle('rotacao-botao');
        opcoesDeAcessibilidade.classList.toggle('apresenta-lista')

    })

    const aumentaFonteBotao = document.getElementById('aumentar-fonte');
    const diminuiFonteBotao = document.getElementById('diminuir-fonte');

    const alternaContraste = document.getElementById('alterna-contraste')

    let tamanhoAtualFonte = 1;

    aumentaFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte += 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    diminuiFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte -= 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    alternaContraste.addEventListener('click', function () {
        document.body.classList.toggle('alto-contraste')
    })

<video controls>
  <source src="video-aula.mp4" type="video/mp4">
  <track src="legendas.vtt" kind="subtitles" srclang="pt" label="Português">
  Seu navegador não suporta o elemento de vídeo.
</video>

<p><a href="transcricao-video.html">Acesse a transcrição completa do vídeo</a></p>
<button onclick="toggleContraste()">Ativar/Desativar Alto Contraste</button>

<script>
  function toggleContraste() {
    document.body.classList.toggle("alto-contraste");
  }
</script>

<style>
  .alto-contraste {
    background-color: black;
    color: yellow;
  }
  .alto-contraste a {
    color: cyan;
  }
</style><a href="#conteudo" class="skip-link">Pular para o conteúdo principal</a>

<style>
  .skip-link {
    position: absolute;
    left: -999px;
    top: auto;
    background: #000;
    color: #fff;
    padding: 8px;
  }
  .skip-link:focus {
    left: 10px;
    top: 10px;
  }
</style>

<main id="conteudo">
  <h1>Bem-vindo ao site acessível</h1>
</main>
<button onclick="aumentarFonte()">A+</button>
<button onclick="diminuirFonte()">A-</button>

<script>
  let tamanho = 16;
  function aumentarFonte() {
    tamanho += 2;
    document.body.style.fontSize = tamanho + "px";
  }
  function diminuirFonte() {
    if (tamanho > 10) {
      tamanho -= 2;
      document.body.style.fontSize = tamanho + "px";
    }
  }
</script><form>
  <label for="nome">Nome:</label>
  <input type="text" id="nome" aria-required="true">

  <label for="email">E-mail:</label>
  <input type="email" id="email" aria-required="true">

  <button type="submit">Enviar</button>
</form><button onclick="toggleDaltonismo()">Simular Daltonismo</button>

<script>
  function toggleDaltonismo() {
    document.body.classList.toggle("daltonismo");
  }
</script>

<style>
  .daltonismo {
    filter: grayscale(100%);
  }
</style>

