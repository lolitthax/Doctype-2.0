<template>
<div>
  <body>
    <app-header />
    <v-parallax
      title="Anúncio do Hackathon"
      dark
      src="../assets/planetas-hackathon.jpg"
      alt="imagem contendo ilustração de planetas e estrelas"
    >
      <h1 class="text-center titulo-parallax">#HACKATHON &lt;!DOCTYPE&gt;</h1>
      <h3 class="text-center sub-parallax">A 12º edição está de outro mundo!</h3>
    </v-parallax>
    <!-- seção que vai o formulário -->
    <section class="contato-section" title="Informação Hackathon">
      <h2 class="section-titulo hackathon-titulo">{Hackathon}</h2>
      <p class="texto">
        Plunct, Plact, Zum! Não haverá #Hackaton algum... se você não se
        inscrever! Apresse-se e garanta seu passaporte para embarcar na 12º Edição.
        <strong>
          Incrições válidas até
          <time datetime="”03-12-2019”">03/12</time>
        </strong>.
      </p>
      <img class="patricio" src="../assets/alien.svg" alt="ícone de um alienígena" />
      <!-- aqui vai um formulário -->
    </section>
    <section class="sobre-section" title="Sobre nós">
      <div class="interior-width">
        <div class="sobre-section-linha">
          <div class="sobre-section-coluna">
            <!-- perguntas frequentes-->
            <section class="sobre" title="Perguntas Frequentes">
              <h2 class="section-titulo">f.a.q.</h2>
              <ul>
                <li class="servico-desc">
                  <p class="servico-titulo">A participação é paga?
                  </p>Não. A participação do evento é gratuita. No entanto, os custos de
                  viagem, estadia e outros fora do evento são de responsabilidade do
                  participante.
                </li>

                <li class="servico-desc">
                  <p class="servico-titulo">
                  O evento é presencial ou online?
                  </p>
                   O Hackathon é presencial. O nosso Q.G é na Av. Antônio Neudenir Benagna Micali,107 Taquaritinga-SP.
                </li>

                <li class="servico-desc">
                  <p class="servico-titulo">Existe um limite de idade para participar?</p>
                  Sim. Uma vez que a nossa intenção é contratar novos profissionais talentosos, limitamos a participação apenas para pessoas com idade superior a 16 anos.
                </li>

                <li class="servico-desc">
                  <p class="servico-titulo">Posso escolher minha equipe?</p>Não. As equipes serão organizadas no dia na hora do evento. Valorizamos o trabalho em equipe independentemente de quem sejam os envolvidos.
                </li>
                <li class="servico-desc">
                  <p>As esquipes serão compostas por quantos integrantes?</p>As equipes terão entre 2 à 5 integrantes no máximo.
                </li>
              </ul>
            </section>
          </div>
          <section class="sobre-section-coluna" title="vídeo da empresa">
            <div class="video" title="vídeo explicativo da empresa">
              <div class="embed">
                <iframe
                  width="560"
                  height="315"
                  src="https://www.youtube.com/embed/OrgpX-_bFqM"
                  frameborder="0"
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                ></iframe>
              </div>
            </div>
          </section>
        </div>
      </div>
    </section>
  </body>
</div>
</template>


<script>
import AppHeader from "../components/AppHeader";
export default {
  data: () => ({}),

  components: {
    AppHeader
  }
};
</script>
<style scoped>

p{
  padding-top:10px;
  font-weight: bold;
}
li{
  list-style: none;
  /* padding-left: 10px; */
}
h2::after {
  content: "|";
  opacity: 1;
  display: inline-block;
  animation: pisca 0.7s infinite;
}
@keyframes pisca {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
}
</style>