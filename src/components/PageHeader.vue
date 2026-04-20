<script setup lang="ts">
import { Divider, LayoutHeader, TypographyTitle } from 'ant-design-vue';
import GeneralDescription from './GeneralDescription.vue';
</script>

<template>
    <LayoutHeader>
        <TypographyTitle class="title font-nea">ПОРТФОЛИО</TypographyTitle>
        <Divider
            orientation="left"
            style="border-color: blue; font-size: 20px"
            type="horizontal"
        >
            <i>обо мне</i>
        </Divider>
        <GeneralDescription></GeneralDescription>
    </LayoutHeader>
</template>

<style scoped>
.ant-layout .ant-layout-header {
    background-color: aliceblue;
    height: auto;
}

.title {
    font-size: 3.5em;
    font-weight: bold;
    margin-top: 0.3em;
    margin-bottom: 0.3em;
}
</style>
