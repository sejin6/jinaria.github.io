<template>
    <div>
        
    </div>
</template>
<script lang="ts">
import { Options,  Vue } from 'vue-class-component';
import Page from './Page'

@Options({
    props: {
        title:String
    },
    
})

export default class Board extends Vue implements Page {
    title!:String
}
</script>
<style lang="scss" scoped>
    
</style>