<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">hanly</h1>
      <h2 class="subtitle">こっちにも「{{ txt }}」</h2>
      <div class="links">
        <nuxt-link to="/test" class="button--green">テストページへ</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  computed: {
    ...mapGetters('test', ['txt'])
  }
}
</script>
