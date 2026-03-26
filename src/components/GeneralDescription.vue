<script setup lang="ts">
import { Col, Flex, Row } from 'ant-design-vue';
import MySkills from './MySkills.vue';
import DescriptionOfMe from './DescriptionOfMe.vue';
</script>
<template>
    <Flex vertical gap="32">
        <DescriptionOfMe></DescriptionOfMe>
        <Row :wrap="false" :gutter="32">
            <Col class="skills-title font-nea"> НАВЫКИ </Col>
            <Col>
                <img class="arrow-img" src="../assets/images/arrow22.png" />
            </Col>
            <Col flex="1">
                <MySkills></MySkills>
            </Col>
        </Row>
    </Flex>
</template>
<style scoped>
.ant-layout .ant-layout-header {
    background-color: aliceblue;
    height: auto;
}
.arrow-img {
    height: 2.5em;
    position: relative;
    transform: rotate(180deg);
    transform: scaleX(-1);
    margin-top: 13px;
}

.skills-title {
    font-size: 2em;
    font-weight: bold;
    margin-left: 16px;
}
</style>
