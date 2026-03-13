<script setup lang="ts">
import imagePython from '../assets/images/skill/python.png';
import imageJavaScript from '../assets/images/skill/js.png';
import imageHTML from '../assets/images/skill/html-5.png';
import imageCSS from '../assets/images/skill/css-3.png';
import imageTypeScript from '../assets/images/skill/typescript.png';
import imageVue from '../assets/images/skill/vue.png';
import imageDjango from '../assets/images/skill/django.png';
import imageSQL from '../assets/images/skill/sql.png';
import imageGitHub from '../assets/images/skill/github.png';
import { Row } from 'ant-design-vue';

const skillList = [
    {
        image: imagePython,
        name: 'Python',
    },
    {
        image: imageJavaScript,
        name: 'JavaScript',
    },
    {
        image: imageTypeScript,
        name: 'TypeScript',
    },
    {
        image: imageCSS,
        name: 'CSS',
    },
    {
        image: imageHTML,
        name: 'HTML',
    },
    {
        image: imageVue,
        name: 'Vue',
    },
    {
        image: imageDjango,
        name: 'Django',
    },
    {
        image: imageSQL,
        name: 'SQL',
    },
    {
        image: imageGitHub,
        name: 'GitHub',
    },
];
</script>

<template>
    <Row justify="space-between">
        <div v-for="skill in skillList" class="skill" :key="skill.name">
            <div class="skill-img">
                <img class="program" :src="skill.image" />
            </div>

            <h3 class="skill-title font-nea">
                {{ skill.name }}
            </h3>
        </div>
    </Row>
</template>

<style scoped>
.skill {
    display: inline-block;
}

.skill-img {
    height: 4em;
    width: 4em;
    border: 0;
    border-radius: 50%;
    border: 2px solid rgb(91, 91, 211);
    box-shadow: 4px 4px 8px rgba(14, 19, 90, 0.4);
    display: flex;
    justify-content: center;
    align-items: center;
    transition: 0.2s linear;
    cursor: pointer;
}

.skill-title {
    margin: 0px;
    text-align: center;
}

.program {
    height: 2.5em;
}

.skill-img:hover {
    box-shadow:
        0 0 0 2px white,
        0 0 0 4px #0e0750;
    transform: translate(0, -3px);
}
</style>
