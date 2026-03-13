<script setup lang="ts">
import { Layout } from 'ant-design-vue';
import MyСontacts from './MyСontacts.vue';
import WorkExperience from './WorkExperience.vue';
</script>

<template>
    <Layout style="background-color: aliceblue">
        <MyСontacts></MyСontacts>
        <WorkExperience></WorkExperience>
    </Layout>
</template>

<style scoped>
.ant-layout {
    /* background-color: rgb(54, 128, 32); */
}

.ant-layout .ant-layout-sider {
    background-color: antiquewhite;
    padding: 16px;
}

.ant-layout .ant-layout-content {
    padding: 16px;
}
</style>
