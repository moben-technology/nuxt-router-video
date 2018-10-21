<template>
  <section>
    <h1>Page d'accueil</h1>
    <br/>
    <br/>
    <p>
      <nuxt-link to="/films"> Consultez les prochaines sorties de films </nuxt-link>
    </p>
  </section>
</template>

<style scoped>
  p {
    text-align: center;
  }

  a {
    text-decoration: underline;
    color: #388070;
  }

  a:hover {
    text-decoration: underline;
    font-weight: bold;
  }

</style>
