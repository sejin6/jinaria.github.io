<template>
  <Header></Header>
  <div class="content">
    <Nav :pages="pages"></Nav>
    <Main msg="hi"></Main>
  </div>
  <Footer></Footer>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Main from './components/Main.vue';
import Nav from './components/Nav.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';


@Options({
  components: {
    Header,
    Main,
    Nav,
    Footer
  },
  data() {
    return {
      pages: [
        '게시판', '방명록'
      ]
    }
  }
})
export default class App extends Vue {
  pages!: []
}
</script>

<style lang="scss">
html {
  height:100%;
}
#app {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 14px;
  position: relative;
  height:100%;
  background-color: #caf8e9;
 
  .content {
    display: flex;
    height: calc(100% - 160px);
  }
  
  
}
</style>
