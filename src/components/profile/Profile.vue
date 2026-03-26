<script setup lang="ts">
import { Layout } from 'ant-design-vue';
import MyСontacts from './MyСontacts.vue';
import WorkExperience from './WorkExperience.vue';
</script>

<template>
    <Layout class="profile">
        <MyСontacts></MyСontacts>
        <WorkExperience></WorkExperience>
    </Layout>
</template>

<style scoped>
.profile {
    background-color: aliceblue;
    padding: 20px 50px 0px 50px;
}
</style>
