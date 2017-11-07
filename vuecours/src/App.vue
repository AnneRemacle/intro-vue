<template>
  <div id="app">
        <page-title :title="title"></page-title>
  </div>
</template>

<script>
    import PageTitle from './PageTitle.vue';

    export default {
      name: 'app',
      components: {
          PageTitle
      },
      data() {
          return {
              title: "Hello World!"
          }
      }
    }
</script>

<!-- on peut se permettre d'écrire juste le nom du component dans les components parce qu'il a le même nom que le fichier -->
