<template>
  <q-page padding class="flex flex-center row">
    <!-- content -->
    <div class="row col-12">
       <q-card bordered class="bg-grey-1 col-12">
      <q-card-section>
        <div class="row items-center no-wrap">
          <div class="col-12">
            <div class="text-h6">TodoList - Login</div>
            </div>
        </div>
      </q-card-section>
      <q-card-section class="row q -col-gutter-md q-pr-none">
        <div class="q-col-gutter-sm col-12 row">
          <q-input class="col-12" filled v-model="user.login" label = "Login" />
          <q-input type="password" class="col-12" filled v-model="user.senha" label="senha" />
        </div>
      </q-card-section>
      <q-card-section class="col-12 text-right">
        <q-btn label="cadastrar" class="q-mr-sm" color="secondary" />
        <q-btn  label="login" @click="logar" color="primary"></q-btn>
      </q-card-section>
    </q-card>
    </div>
  </q-page>
</template>
<script>
export default {
  // name: 'PageName',
  data () {
    return {
      user: {
        login: '',
        senha: ''
      }
    }
  },
  methods: {
    logar () {
      this.$q.notify({
        message: 'Usuario Logado com sucesso',
        color: 'positive'
      })
      this.$router.push('/')
    }
  }
}
</script>
