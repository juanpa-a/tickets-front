<template>
  <v-app id="app">
    <Header />
        <v-container>
            <Events />
        </v-container>
    <Footer />
  </v-app>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'
import Events from './components/Events'
import Login  from './components/Login'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Events,
    Login
  },
  data () {
    return {
      //
    }
  }
}
</script>
