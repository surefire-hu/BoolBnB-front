<script>
/* 
  Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
  1) Importazione del componente
  2) Dichiarazione del componente
  3) Utilizzo del componente
*/
// 1) Importazione del componente
import AppHeader from './components/AppHeader.vue';

export default {
  data() {
    return { 
      count: 0
    }
  },
  // 2) Dichiarazione del componente
  components: {
    AppHeader
  },
  methods: {
    incrementCount() {
      this.count++;
    }
  }
}
</script>

<template>
  <div>
    <!-- 3) Utilizzo del componente -->
    <AppHeader />
    
    <main>
      <button @click="incrementCount()" class=" border-dashed border-black border-2">
        {{ count }}
      </button>
    </main>
  </div>
</template>

<style scoped>
main {
  text-align: center;
}
</style>