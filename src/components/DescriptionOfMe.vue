<script setup lang="ts">
import { Col, Row } from 'ant-design-vue';
import MyPhoto from './MyPhoto.vue';
</script>
<template>
    <Row :wrap="false" :gutter="32" align="bottom">
        <Col>
            <MyPhoto></MyPhoto>
        </Col>
        <Col class="info font-nea">
            <img class="work-img" src="../assets/images/work.png" />
            <p style="margin: 10px">
                Меня зовут Анастасия<br />
                Я Junior - программнст, знаю языки программирования как Python,
                Java Script. Имею опыт в коммерческой разработке с Vue более
                года. Способна работать как индивидульно, так и в команде. Как
                человек ориентированный на развитие, моя основная цель -
                предоставлять выполненную работу (программный код) высокого
                уровня.
            </p>
        </Col>
    </Row>
</template>
<style scoped>
.info {
    background-color: rgb(91, 91, 211);
    border-radius: 40px 40px 40px 0;
    color: aliceblue;
    font-size: medium;
    padding: 5px;
    line-height: 30px;
    display: flex;
    justify-content: flex-end;
}

.work-img {
    height: 2.5em;
    position: absolute;
}
</style>
