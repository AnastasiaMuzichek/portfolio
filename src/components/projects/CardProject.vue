<script setup lang="ts">
import {
    Card,
    Col,
    Flex,
    Row,
    Space,
    TypographyParagraph,
    TypographyTitle,
} from 'ant-design-vue';
import ProjectPhoto from './ProjectPhoto.vue';
import type { PropType } from 'vue';
import type { ProjectValue } from '../../types';

defineProps({
    name: {
        required: true,
        type: String as PropType<ProjectValue['name']>,
    },
    description: {
        required: true,
        type: String as PropType<ProjectValue['description']>,
    },
    image: {
        required: true,
        type: String as PropType<ProjectValue['image']>,
    },
    language: {
        required: true,
        type: String as PropType<ProjectValue['language']>,
    },
    stack: {
        required: true,
        type: String as PropType<ProjectValue['stack']>,
    },
    linkWebsite: {
        required: true,
        type: String as PropType<ProjectValue['linkWebsite']>,
    },
    linkCode: {
        required: true,
        type: String as PropType<ProjectValue['linkCode']>,
    },
});
</script>

<template>
    <Card class="card-project">
        <Row>
            <Col :span="10">
                <ProjectPhoto
                    :image="image"
                    :language="language"
                ></ProjectPhoto>
            </Col>
            <Col class="font-nea" :span="14">
                <Flex class="h-100" justify="space-between" vertical>
                    <TypographyTitle
                        :level="5"
                        class="project-title font-nea"
                        >{{ name }}</TypographyTitle
                    >
                    <TypographyParagraph class="text-description font-nea">{{
                        description
                    }}</TypographyParagraph>
                    <TypographyParagraph
                        class="text-description font-nea"
                        style="font-size: 17px"
                    >
                        Основной используемый стек: {{ stack }}
                    </TypographyParagraph>
                    <Space>
                        <a
                            v-if="linkWebsite !== ''"
                            :href="linkWebsite"
                            class="button-link font-nea"
                            target="_blank"
                            title="Перейти на сайт и посмотреть запущенный проект"
                        >
                            Посмотреть проект
                        </a>
                        <a
                            :href="linkCode"
                            class="button-link font-nea"
                            target="_blank"
                            title="Перейти на сайт и посмотреть запущенный проект"
                        >
                            Посмотреть программый код проекта
                        </a>
                    </Space>
                </Flex>
            </Col>
        </Row>
    </Card>
</template>

<style scoped>
h5.ant-typography {
    margin-block-start: 0.5em;
}

.card-project {
    border-color: rgb(91, 91, 211);
    border-width: 2px;
    font-size: 16px;
    width: 100%;
}

.project-title {
    font-size: 2em;
    font-weight: bold;
    margin-left: 16px;
    /* text-decoration: underline;
    text-decoration-style: dashed;
    text-decoration-thickness: 3px;
    text-decoration-color: rgb(91, 91, 211); */
}
.text-description {
    font-size: 15px;
}
.button-link {
    display: inline-block;
    padding: 5px 10px;
    background-color: rgb(91, 91, 211);
    color: white;
    text-decoration: none;
    border-radius: 4px;
    font-size: 16px;
}

.button-link:hover {
    background-color: rgba(14, 19, 90);
}
</style>
