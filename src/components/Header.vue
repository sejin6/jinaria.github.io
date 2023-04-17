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
        text-align: center;
        vertical-align:baseline;
        padding: 40px 0 80px 0;
        height: 80px;
        color: $text-color;
        font-family: cursive;
        font-weight: bold;
    }
</style>