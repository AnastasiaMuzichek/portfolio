<script setup lang="ts">
import { Flex, LayoutSider, Space, Tag } from 'ant-design-vue';

const hobbys = [
    'рисование',
    'музыка',
    'аниме',
    'баскетбол',
    'прогулки',
    'гейминг',
    'вязание',
];
</script>

<template>
    <LayoutSider style="background-color: aliceblue">
        <Tag color="rgb(91, 91, 211)" class="font-nea" style="font-size: 20px"
            >МОИ ИНТЕРЕСЫ</Tag
        >
        <Flex vertical gap="10" style="margin-top: 20px">
            <Space v-for="hob in hobbys">{{ hob }}</Space>
        </Flex>
    </LayoutSider>
</template>

<style scoped></style>
