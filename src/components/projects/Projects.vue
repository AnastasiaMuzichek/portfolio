<script setup lang="ts">
import { Flex, Space, Tag } from 'ant-design-vue';

const projects = [
    {
        name: 'heroes',
        description:
            'Сайт посвящен тематике игры Heroes of Might and Magic 3: \
             In the Wake of Gods, где описаны боевые командиры отрядов.',
        link: 'https://anastasiamuzichek.github.io/heroes/',
    },
    {
        name: 'api-dwarfs',
        description:
            'Данный проект представляет собой api по получению и сохранению \
            гномов(персонажей) и связанных с ними оружий. Функционал обработчиков \
            реализован на базе GenericView',
        link: 'https://github.com/AnastasiaMuzichek/api-dwarfs',
    },
];
</script>

<template>
    <Tag
        color="rgb(91, 91, 211)"
        class="font-nea"
        style="font-size: 20px; margin-top: 30px"
        >МОИ ПРОЕКТЫ НА GIT</Tag
    >
    <Flex vertical gap="10" style="margin-top: 20px">
        <Space v-for="project in projects">
            <p>
                <a :href="project.link" target="_blank"
                    >Приложение {{ project.name }}</a
                >
                -
                {{ project.description }}
            </p>
        </Space>
    </Flex>
</template>

<style scoped></style>
