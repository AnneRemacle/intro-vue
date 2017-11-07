<template>
  <div id="app">
        <page-title :title="title"></page-title>
  </div>
</template>

<script>
    import PageTitle from './PageTitle.vue';
    import { bus } from "./main.js";

    export default {
      name: 'app',
      components: {
          PageTitle
      },
      data() {
          return {
              title: "Hello World!"
          }
      },
      methods: {
          clearTitle() {
              this.title = '';
          }
      },
      created() {
          bus.$on('clearTitle', this.clearTitle );
      }
    }
</script>
<!-- created() {
    bus.$on('clearTitle')
}
on dit au bus d'écouter cet événement quand le composant est créé
emit envoie un événement
on écoute un événement -->
<!-- on peut se permettre d'écrire juste le nom du component dans les components parce qu'il a le même nom que le fichier -->
