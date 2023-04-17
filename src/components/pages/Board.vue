<template>
    <div>
        
    </div>
</template>
<script lang="ts">
import { Options,  Vue } from 'vue-class-component';
import Page from './Page'

@Options({
    props: ['title'],
    
})

export default class Board extends Vue implements Page {
    title!: String
    contents!: String
}
</script>
<style lang="scss" scoped>
    
</style>