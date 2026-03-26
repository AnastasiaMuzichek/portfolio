<script setup lang="ts">
import { LayoutSider, Tag } from 'ant-design-vue';
import ListHobbys from './ListHobbys.vue';
</script>

<template>
    <LayoutSider class="padding-hobby">
        <Tag color="rgb(91, 91, 211)" class="font-nea text-hobby"
            >Мои интересы</Tag
        >
        <ListHobbys></ListHobbys>
    </LayoutSider>
</template>

<style scoped>
.padding-hobby {
    background-color: aliceblue;
    border: 2px solid rgb(91, 91, 211);
    border-radius: 15px;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 450px;
}

.text-hobby {
    font-size: 20px;
    position: absolute;
    top: -10px;
    left: 35px;
    height: 20px;
    width: 130px;
    background-color: pink;
    text-align: center;
}
</style>
