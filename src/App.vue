<template>
  <Header></Header>
  <div class="content">
    <Nav :pages="pages" @moveToLink="moveToLink"></Nav>
    <Main :msg="currentPage"></Main>
  </div>
  <Footer></Footer>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Main from './components/Main.vue';
import Nav from './components/Nav.vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Page from './components/pages/Page';


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
      ],
      currentPage: '게시판'
    }
  }
})
export default class App extends Vue {
  pages!: Array<Page>
  currentPage!: String
  moveToLink(event: Event, link: String) {
    console.log(`say ${link}`);
    this.currentPage = link;
  }
}
</script>

<style lang="scss">
@import '../static/common.scss';

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
  background: no-repeat url('../static/milkyway.jpg');
  background-size: 100% 100%;
 
  .content {
    display: flex;
    height: calc(100% - 160px);
    border-bottom: 1px solid $border-color;
  }
  
  
}
</style>
