<template>
    <div class="header">
        Jinaria's Blog
    </div>
</template>

<script lang="ts">
import {Options, Vue} from 'vue-class-component';


@Options({

})

export default class Header extends Vue {
    
}
</script>

<style scoped lang="scss">
@import '../../static/common.scss';
    .header {
        font-size: 32px;
        text-align: right;
        vertical-align:baseline;
        padding: 20px 20px 0 0;
        height: 80px;
        color: $text-color;
        font-family: cursive;
        border-bottom: $border-color solid 2px;
        font-weight: bold;
    }
</style>