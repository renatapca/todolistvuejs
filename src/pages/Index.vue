<template>
  <q-page padding>
    <div class="text-h4 q-mb-md">Listas</div>
    <q-list>
      <q-item v-for="lista in listas" :key="lista.id" clickable v-ripple class="shadow-2 q-mb-sm">
        <q-item-section avatar>
          <q-icon color="primary" name="check" />
        </q-item-section>
        <q-item-section>{{ lista.title }}</q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
export default {
  name: 'MinhasListas',
  data () {
    return {
      listas: []
    }
  },
  methods: {
    loadListas () {
      this.$axios.get('https://jsonplaceholder.typicode.com/user/1/todos').then(response => {
        this.listas = response.data
      })
    }
  },
  beforeMount () {
    this.loadListas()
  }
}
</script>
