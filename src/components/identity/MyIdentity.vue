<script setup lang="ts">
import { Layout } from 'ant-design-vue';
import MyHobby from './MyHobby.vue';
import MyAbilities from './MyAbilities.vue';
</script>

<template>
    <Layout class="layout-identity">
        <MyHobby></MyHobby>
        <MyAbilities></MyAbilities>
    </Layout>
</template>

<style scoped>
.layout-identity {
    background-color: aliceblue;
    padding: 20px 50px 0px 50px;
}
</style>
