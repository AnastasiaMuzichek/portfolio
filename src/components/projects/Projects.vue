<script setup lang="ts">
import { LayoutContent, Tag } from 'ant-design-vue';
import CardProject from './CardProject.vue';
import imageHeroes from '../../assets/images/projects/heroes.png';
import imageDwarf from '../../assets/images/projects/dwarf.png';
import imageGame from '../../assets/images/projects/game.png';
import imageTeachers from '../../assets/images/projects/teachers.png';
import imageDwarfs from '../../assets/images/projects/dwarfs.png';
import imageConway from '../../assets/images/projects/conway.png';
import type { ProjectValue } from '../../types';

const projects: ProjectValue[] = [
    {
        name: 'heroes',
        description:
            'Сайт посвящен тематике игры Heroes of Might and Magic 3: \
             In the Wake of Gods, с подробными карточками командиров: фото, указание \
             города, расового умения, уникального навыка и заклинания. Для каждого героя \
             реализован отдельный профиль с индивидуальным описанием характеристик.',
        image: imageHeroes,
        language: 'vue',
        stack: 'TypeScript, Vue, CSS, HTML',
        linkWebsite: 'https://anastasiamuzichek.github.io/heroes/',
        linkCode: 'https://github.com/AnastasiaMuzichek/heroes',
    },
    {
        name: 'api-teachers',
        description:
            'Разработала REST API для управления данными учеников и учителей с возможностью добавления, \
            редактирования, удаления и поиска по различным критериям (имя, фамилия, отчество, оценка, \
            дисциплина). Реализована автоматическая привязка учеников к учителям по преподаваемым \
            дисциплинам и группировка в классы.',
        image: imageTeachers,
        language: 'python',
        stack: 'Python',
        linkWebsite: '',
        linkCode: 'https://github.com/AnastasiaMuzichek/api-teachers',
    },
    {
        name: 'app-games',
        description:
            'Веб-приложение - каталог игр с авторизацией, где пользователи могут добавлять \
            свои игры, оставлять комментарии и ставить оценки. Каждая игра представлена в виде \
            карточки с фото (стандартный набор картинок - зависит отжанра игры), названием, жанром и годом \
            выпуска, а для оценки и комментирования реализовано всплывающее окно. \
            стек: TypeScript + Vue3 + HTML + CSS',
        image: imageGame,
        language: 'vue',
        stack: 'Vue, TypeScript, CSS, HTML',
        linkWebsite: 'https://anastasiamuzichek.github.io/app-games/#/',
        linkCode: 'https://github.com/AnastasiaMuzichek/app-games',
    },
    {
        name: 'api-dwarfs',
        description:
            'Создала REST API для управления данными о гномах и их оружия, с возможностью создания, \
            получения, изменения и удаления гномов и связанных с ними оружий.\
            Функционал обработчиков реализован на базе GenericView.',
        image: imageDwarf,
        language: 'python',
        stack: 'Python',
        linkWebsite: '',
        linkCode: 'https://github.com/AnastasiaMuzichek/api-dwarfs',
    },
    {
        name: 'dwarfs',
        description:
            '«Кадровый центр "Маленькие мастера"» — интерактивный сайт для найма гномов, \
                где каждый кандидат представлен в виде карточки с личными данными, навыками и оружием. \
                Пользователь может просматривать, добавлять, редактировать и удалять карточки гномов, \
                а также детально изучать характеристики каждого работника (есть отдельное подробное \
                описание и фото оружия).',
        image: imageDwarfs,
        language: 'vue',
        stack: 'TypeScript, Vue, CSS, HTML',
        linkWebsite: 'https://anastasiamuzichek.github.io/dwarfs/',
        linkCode: 'https://github.com/AnastasiaMuzichek/dwarfs',
    },
    {
        name: 'conway-game',
        description:
            '«Живая клетка» — интерактивный клеточный автомат, где пользователь задаёт начальное \
            состояние, а затем наблюдает за эволюцией системы. Цвет каждой клетки динамически \
            отражает её текущее состояние, создавая наглядную визуализацию процессов развития.',
        image: imageConway,
        language: 'vue',
        stack: 'Vue, CSS, HTML, TypeScript',
        linkWebsite: 'https://anastasiamuzichek.github.io/conway-game/',
        linkCode: 'https://github.com/AnastasiaMuzichek/conway-game',
    },
];
</script>

<template>
    <LayoutContent class="project-laoyt">
        <Tag color="rgb(91, 91, 211)" class="font-nea text-project"
            >Мои проекты на Github</Tag
        >
        <CardProject
            v-for="project in projects"
            :name="project.name"
            :description="project.description"
            :image="project.image"
            :language="project.language"
            :stack="project.stack"
            :linkWebsite="project.linkWebsite"
            :linkCode="project.linkCode"
            style="margin-top: 20px; display: block"
        >
        </CardProject>
        <a
            href="https://github.com/AnastasiaMuzichek?tab=repositories"
            target="_blank"
            class="btn-github"
        >
            <div class="btn-github-triangle"></div>
            <div class="btn-github-content font-nea">Больше проектов тут</div>
        </a>
    </LayoutContent>
</template>

<style scoped>
.project-laoyt {
    background-color: aliceblue;
    padding-left: 16px;
    padding-right: 16px;
    border: 2px rgb(91, 91, 211);
    border-style: solid none none none;
    position: relative;
    display: block;
}

.text-project {
    font-size: 20px;
    margin-top: 30px;
    position: absolute;
    top: -40px;
    left: 216px;
    height: 20px;
    width: 200px;
    text-align: center;
}
.btn-github {
    display: flex;
    align-items: center;
    justify-content: end;
    margin-top: 20px;
    cursor: auto;
}

.btn-github-triangle {
    border-top: 40px solid transparent;
    border-bottom: 40px solid transparent;
    border-right: 40px solid rgb(91, 91, 211);
    box-shadow: 4px 0px rgba(14, 19, 90, 0.2);
    cursor: pointer;
}
.btn-github-content {
    background-color: rgb(91, 91, 211);
    color: white;
    font-size: 16px;
    padding: 8px;
    box-shadow: 4px 4px 8px rgba(14, 19, 90, 0.4);
    cursor: pointer;
}
</style>
