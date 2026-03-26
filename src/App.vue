<script setup lang="ts">
import { Layout, LayoutFooter } from 'ant-design-vue';
import PageHeader from './components/PageHeader.vue';
import Profile from './components/profile/Profile.vue';
import MyIdentity from './components/identity/MyIdentity.vue';
import Projects from './components/projects/Projects.vue';
</script>

<template>
    <Layout>
        <PageHeader></PageHeader>

        <Profile></Profile>

        <MyIdentity></MyIdentity>
        <LayoutFooter style="background-color: aliceblue">
            <Projects></Projects>
        </LayoutFooter>
    </Layout>
</template>
