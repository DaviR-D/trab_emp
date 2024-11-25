<template>
  <div class="time-control">
    <h1>Controle de Tempo de Uso do Celular e Internet</h1>

    <section>
      <h2>Por que é importante controlar o tempo de tela?</h2>
      <p>
        No mundo atual, o uso do celular e da internet é quase inevitável. Estes recursos nos
        conectam ao mundo, facilitam o trabalho, o aprendizado e nos entretem. No entanto, o uso
        excessivo pode trazer consequências negativas, como dificuldades de concentração, redução do
        tempo para atividades físicas e até problemas de saúde mental, como ansiedade e estresse.
        Por isso, controlar o tempo de uso do celular e internet é fundamental para manter uma vida
        equilibrada.
      </p>
    </section>

    <section>
      <h2>Benefícios do Controle de Uso</h2>
      <ul>
        <li>
          <strong>Melhora na qualidade do sono:</strong> Limitar o tempo de tela, especialmente
          antes de dormir, ajuda o corpo a relaxar e se preparar para uma boa noite de sono.
        </li>
        <li>
          <strong>Aumento da produtividade:</strong> Reduzir o tempo em redes sociais e aplicativos
          de entretenimento libera tempo para tarefas importantes e reduz a procrastinação.
        </li>
        <li>
          <strong>Redução da ansiedade:</strong> Menos tempo de exposição a notícias e redes sociais
          pode reduzir o estresse e a ansiedade causados pela comparação e sobrecarga de
          informações.
        </li>
        <li>
          <strong>Mais tempo para atividades físicas e sociais:</strong> Passar menos tempo no
          celular abre espaço para atividades saudáveis e interações face a face.
        </li>
      </ul>
    </section>

    <section>
      <h2>Dicas para Controlar o Tempo de Uso</h2>
      <ol>
        <li>
          <strong>Defina metas de uso diário:</strong> Estabeleça um limite de tempo para o uso de
          aplicativos específicos ou para o uso total do celular. Muitos dispositivos têm
          configurações de controle de tempo de tela.
        </li>
        <li>
          <strong>Use aplicativos de monitoramento:</strong> Existem diversos aplicativos que ajudam
          a monitorar o tempo de uso e definir limites, como o <i>Moment</i> e o <i>Screen Time</i>.
        </li>
        <li>
          <strong>Desative notificações desnecessárias:</strong> Notificações constantes podem
          interromper o foco e incentivar o uso excessivo. Desativá-las reduz o número de vezes que
          pegamos o celular.
        </li>
        <li>
          <strong>Reserve momentos sem celular:</strong> Tente criar "zonas livres de celular" em
          horários específicos, como durante as refeições ou antes de dormir.
        </li>
        <li>
          <strong>Invista em hobbies offline:</strong> Dedique tempo para atividades que não
          envolvam tecnologia, como leitura, esportes, artes ou encontros com amigos e família.
        </li>
      </ol>
    </section>

    <section>
      <h2>Considerações Finais</h2>
      <p>
        Controlar o tempo de uso do celular e internet é um passo importante para uma rotina mais
        saudável e equilibrada. Ao estabelecer limites e criar hábitos conscientes, podemos usar a
        tecnologia de forma produtiva e benéfica, sem permitir que ela interfira em nosso bem-estar
        e em nossos relacionamentos. Pequenas mudanças podem fazer uma grande diferença na qualidade
        de vida, proporcionando mais tempo para o que realmente importa.
      </p>
    </section>
  </div>
</template>

<script>
export default {
  name: "TimeControl",
};
</script>

<style scoped>
.time-control {
  max-width: 900px;
  margin: auto;
  padding: 20px;
  border-radius: 15px;
  background: #f0f4f8;
  color: #333;
  font-family: "Arial", sans-serif;
  line-height: 1.8;
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

h1 {
  font-size: 2.2em;
  text-align: center;
  color: #007bff;
  margin-bottom: 30px;
}

h2 {
  font-size: 1.6em;
  color: #0056b3;
  margin-top: 20px;
  margin-bottom: 10px;
  border-bottom: 2px solid #007bff;
  padding-bottom: 5px;
}

p {
  font-size: 1.1em;
  margin-bottom: 15px;
}

ul,
ol {
  margin: 20px 0;
  padding-left: 20px;
}

ul li,
ol li {
  margin-bottom: 10px;
  line-height: 1.6;
}

strong {
  color: #0056b3;
}

section {
  margin-bottom: 20px;
}

i {
  color: #007bff;
}

@media (max-width: 768px) {
  .time-control {
    padding: 15px;
  }

  h1 {
    font-size: 1.8em;
  }

  h2 {
    font-size: 1.4em;
  }

  p,
  ul li,
  ol li {
    font-size: 1em;
  }
}
</style>
