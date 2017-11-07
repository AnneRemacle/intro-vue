<template>
  <h1>{{ title }}</h1>
</template>

<script>
    export default {
      name: "page-title",
      props: [
          'title'
      ]
    }
</script>

<!-- on définit une prop qui est une sorte de porte d'entrée entre le parent et l'enfant -->
