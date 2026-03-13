<script setup lang="ts">
import { LayoutContent, Tag, Flex, Space } from 'ant-design-vue';

const abilities = [
    'работоспособность',
    'коммуникабельность',
    'обучаемость',
    'стрессоустойчивость',
    'навыки межличностногого общения',
    'организационные навыки',
    'точность и внимательность к деталям',
];
</script>

<template>
    <LayoutContent style="background-color: aliceblue">
        <Tag color="rgb(91, 91, 211)" class="font-nea" style="font-size: 20px"
            >МОИ НАВЫКИ</Tag
        >
        <Flex vertical gap="10" style="margin-top: 20px">
            <Space v-for="abilitie in abilities">{{ abilitie }}</Space>
        </Flex>
    </LayoutContent>
</template>

<style scoped></style>
