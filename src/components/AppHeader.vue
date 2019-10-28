<template>
<div>
  <head>
    <meta charset="utf-8" />
    <title>!Doctype</title>
    <meta
      name="author"
      content="Aline Iasmim, Daphne Helena, Luis Fernando, Pricila Agda, José Airton"
    />
    <meta
      name="description"
      content="Seja bem-vindo a <!Doctype! Nós te ajudamos a alcançar objetivos futuros com o uso da tecnologia. Telefone(16)99165-2578."
    />
    <meta
      name="keywords"
      content="Doctype, Hackathon Doctype, Aline Damião, Daphne Helena, 
      Priscila Agda, José Airton, Luís Fante, Desenvolvimento de Apps ,Acessibilidade,
      Criação de Sites, Webdesign, SEO, Inteligência Artificial,
      Hackathon 2019, Soluções digitais Taquaritinga, Empresa de desenvolvimento Taquaritinga."
    />
    <link rel="stylesheet" href="style.css" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.1/css/all.css" />
  </head>
  <body>
    <header>
      <nav>
  <a href="/" >
        <img
          class="logo"
          src="../assets/logo_doctype.svg"
          alt="logotipo da empresa Doctype"
          title="<!DOCTYPE>"
        />
      </a>

      <input type="checkbox" id="chk" />
      <label for="chk" class="show-menu-btn">
        <i class="fas fa-bars"></i>
      </label>

      <ul class="menu">
        <a style="color:white;" href="/" title="Início">Início</a>
        <a style="color:white;" href="paginas/projetos" title="Projetos">Projetos</a>
        <a style="color:white;" href="/paginas/hackathon" title="Hackathon">Hackathon</a>
        <a style="color:white;" href="/sobre" title="Sobre">Sobre</a>
        <a style="color:white;" href="/paginas/contato" title="Contato">Contato</a>
        <a style="color:white;" href="/painel/login" title="Login">Login</a>
        <label for="chk" class="hide-menu-btn">
          <i class="fas fa-times"></i>
        </label>
      </ul>
      </nav>
    
    </header>
  </body>
</div>
</template>
<script>
export default {};
</script>

<style>
header {
  height: 100px;
  background: black;
  padding: 0 20px;
  color: #fff;
  display: flex;
}
.logo {
  line-height: 100px;
  justify-content: left;
  height: 100%;
  width: 90px;
}

.menu {
  float: right;
  line-height: 100px;
}
.menu a {
  text-transform: uppercase;
  text-decoration: none;
  padding: 0 10px;
  transition: 0.4s;
}

.show-menu-btn,
.hide-menu-btn {
  transition: 0.4s;
  font-size: 30px;
  cursor: pointer;
  display: none;
}
.show-menu-btn {
  float: right;
}
.show-menu-btn i {
  line-height: 100px;
}

#chk {
  position: absolute;
  visibility: hidden;
  z-index: -1111;
}

@media screen and (max-width: 800px) {
  .show-menu-btn,
  .hide-menu-btn {
    display: flex;
  }
  .menu {
    z-index: 2;
    position: absolute;
    width: 100%;
    height: 500px;
    background: black;
    right: -100%;
    top: 0;
    text-align: center;
    padding: 80px 0;
    line-height: normal;
    transition: 0.7s;
  }
  .menu a {
    display: block;
    padding: 20px;
  }
  .hide-menu-btn {
    position: absolute;
    top: 40px;
    right: 40px;
  }
  #chk:checked ~ .menu {
    right: 0;
  }

  .v-parallax {
    position: relative;
    z-index: -12000;
  }
}
</style>