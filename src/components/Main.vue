<template>
    <div class="main">{{ msg }}</div>
</template>

<script lang="ts">
import {Vue, Options} from 'vue-class-component';

@Options({
  props: {
    msg: String
  }
})

export default class Main extends Vue {
    msg!: string
}
</script>

<style scoped>
    .main {
        
    }
</style>