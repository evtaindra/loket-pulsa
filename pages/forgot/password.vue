<template>
  <section class="container">
    <div class="content">
      <h1 class="title">
        NUXT
      </h1>
      <form @submit.prevent="login">
        <div class="form-group">
          <input v-model="email" type="email" class="form-control" aria-describedby="emailHelp" placeholder="Enter email">
          <div class="invalid-feedback">
            Please choose a email.
          </div>
        </div>
      
        <button type="submit" class="btn btn-secondary btn-block" >Kirim Permintaan</button>
      </form>
      <div class="mt-5 mb-4">
        <a class="btn btn-outline-light" href="/auth/login">Login Sekarang</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      password: "",
      ip: 0,
      loading: false
    }
  },
  mounted() {},
  methods: {
    async login() {
      // const { email, password } = this
      // const data = await this.$axios.$post('https://api-sm.s45.in/me/login', {email, password})
      // this.ip = data
      // console.log(this.ip)
      this.$toast.success("Logging in...").goAway(1500)
    }
  }
}
</script>

<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.content {
  width: 100%;
  margin: 50px;
}
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 60px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 20px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
