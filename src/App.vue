<template>
  <Header></Header>
  <Nav :pages="pages" @moveToLink="moveToLink" :currentPage="currentPage"></Nav>
  <Main :currentPage="currentPage"></Main>
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
      pages: getPageList(),
      currentPage: {
        title: '자기소개',
        contents: '저는 진승기입니다.'
      }
    }
  }
})
export default class App extends Vue {
  pages!: Array<Page>
  currentPage!: Page
  moveToLink(event: Event, link: Page) {
    console.log(`say ${link.title}`);
    this.currentPage = link;
  }
  
}

function getPageList(): Page[] {
  return [
    {
      title: '자기소개',
      contents: '저는 진승기입니다.'
    },
    {
      title: '역사',
      contents: '95년생'
    }
  ];
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

  border-bottom: 1px solid $border-color;
  
  
  
}
</style>
