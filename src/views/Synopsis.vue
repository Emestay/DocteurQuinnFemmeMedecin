<template>
  <div class="synopsis">
    <h1>Synopsis</h1>
    <p>
      Docteur Quinn, femme médecin est une série télévisée américaine en 150
      épisodes de 44 minutes, créée par Beth Sullivan et diffusée entre le 1ᵉʳ
      janvier 1993 et le 16 mai 1998 sur le réseau CBS. En France, la série a
      été diffusée à partir du 22 août 1993 sur M6 puis rediffusée sur Téva,
      TV Breizh, RTL9 et 6ter. Au Québec, elle a été diffusée sur TVA.
    </p>
    <p>
      Dans cette série, Michaela Quinn est une femme médecin de Boston qui
      décide de s'installer à Colorado Springs dans les années 1860 pour
      exercer son métier et ainsi venir en aide à une population dans le
      besoin. Elle doit faire face aux préjugés de l'époque et prouver ses
      compétences à une population réticente à accepter une femme médecin.
      Malgré les obstacles, elle parvient à se faire respecter et à gagner la
      confiance des habitants de la ville.
    </p>
  </div>
</template>

<script>
export default {
  name: 'Synopsis',
};
</script>

<style scoped>
.synopsis {
  font-family: 'Comic Sans MS', sans-serif;
  background-color: #c0c0c0;
  padding: 20px;
  border: 2px solid #ffcc00;
  border-radius: 10px;
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  max-width: 800px;
  margin: 20px auto;
}

.synopsis h1 {
  font-size: 24px;
  text-align: center;
  color: #ff9900;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
}

.synopsis p {
  font-size: 14px;
  text-align: justify;
  color: #000;
}
</style>
