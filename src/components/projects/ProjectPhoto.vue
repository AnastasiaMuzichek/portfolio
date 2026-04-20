<script setup lang="ts">
import { computed } from 'vue';
import iconVue from '../../assets/images/skill/vue.png';
import iconPython from '../../assets/images/skill/python.png';
import type { PropType } from 'vue';
import type { ProjectValue } from '../../types';

const props = defineProps({
    image: {
        required: true,
        type: String as PropType<ProjectValue['image']>,
    },
    language: {
        required: true,
        type: String as PropType<ProjectValue['language']>,
    },
});

const imageSkill = computed(() =>
    props.language === 'vue' ? iconVue : iconPython,
);
const title = computed(() => {
    const value = props.language === 'vue' ? 'Vue3' : 'Python';
    return `Проект был написан на ${value}`;
});
</script>

<template>
    <div style="position: relative; display: block; margin-top: 20px">
        <div class="project-img" :title="title">
            <img class="program" :src="imageSkill" />
        </div>
        <img class="photo-project" :src="props.image" />
    </div>
</template>

<style scoped>
.photo-project {
    height: 200px;
    width: 420px;
    border: 3px solid rgb(91, 91, 211);
    border-radius: 20px;
}
.project-img {
    height: 3em;
    width: 3em;
    border: 0;
    border-radius: 50%;
    border: 5px solid rgb(91, 91, 211, 0.8);
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    position: absolute;
    top: -10px;
    left: 398px;
    background-color: white;
}

.program {
    height: 1.8em;
}
</style>
