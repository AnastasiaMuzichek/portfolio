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
                Я — начинающий программист (Junior), владею современными языками
                программирования, такими как Python и JavaScript. Обладаю опытом
                коммерческой разработки на Vue.js более года. Уверенно работаю
                как самостоятельно, так и в команде. Стремлюсь к постоянному
                профессиональному росту и ставлю перед собой задачу — создавать
                качественный, чистый и поддерживаемый программный код,
                соответствующий высоким стандартам индустрии.
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
