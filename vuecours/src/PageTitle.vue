<template>
    <div>
        <h1>{{ title }}</h1>

        <button @click="emptyTitle()">Reset</button>

        <slot>
            <p>Le contenu par défaut</p>
        </slot>
    </div>
</template>

<script>
    import { bus } from './main.js';

    export default {
      name: "page-title",
      props: {
        title: {
            required: true,
            type: String
         }
     },
     methods: {
         emptyTitle() {
            bus.$emit( 'clearTitle' );
             }
        }
     };
</script>

<!-- on définit une prop qui est une sorte de porte d'entrée entre le parent et l'enfant -->
<!-- pour faire une action dans l'enfant qui affecte le parent, il faut utiliser un événement personnalisé dans la méthode -->
<!-- $emit enregistre cleartitle comme un nouveau type d'événement qu'on peut utiliser -->

<style scoped >
    h1 {
        font-family: "Helvetica Neue", "Arial", "sans serif";
        color: darkred;
    }
</style>
