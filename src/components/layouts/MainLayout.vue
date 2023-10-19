<template>
    <div class="main-layout">
        <HeaderComp/>
        <slot name="content"/>
        <FooterComp/>
    </div>
</template>

<script>
import HeaderComp from "../../components/HeaderComp.vue";
import FooterComp from "../../components/FooterComp.vue";
export default {
    name: 'MainLayout',
    components: {HeaderComp, FooterComp }
}
</script>

<style lang="scss">
    .main-layout {
        display: flex;
        flex-direction: column;
        width: 1440px;
    }
</style>