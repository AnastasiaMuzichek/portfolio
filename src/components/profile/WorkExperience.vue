<script setup lang="ts">
import { LayoutContent, Tag } from 'ant-design-vue';
import CardWork from './CardWork.vue';

const experience = [
    {
        date: '2021 - 2022',
        company: 'Codica',
        description: 'Преподователь программирования',
    },
    {
        date: '2021 -  2022',
        company: 'Codica | Преподователь программирования',
        description:
            'преподавание дисциплин детям (программмирование на Python, Scratch, \
            game design, Minecraft, компьютерная грамотность)',
    },
];
</script>

<template>
    <LayoutContent>
        <Tag
            color="rgb(91, 91, 211)"
            class="font-nea"
            style="font-size: 20px; padding: 15px"
            >Опыт работы</Tag
        >
        <CardWork
            v-for="value in experience"
            :date="value.date"
            :company="value.company"
            :description="value.description"
        ></CardWork>
    </LayoutContent>
</template>

<style scoped>
.ant-layout .ant-layout-content > * {
    margin-bottom: 16px;
}
</style>
