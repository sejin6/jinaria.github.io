<template>
    <div class="footer">
        Footer
    </div>
</template>
<script lang="ts">
import {Options, Vue} from 'vue-class-component';

@Options({

})

export default class Footer extends Vue {
    
}
</script>
<style lang="scss" scoped>
    .footer {
        background-color: green;
        height: 80px;
    }
</style>