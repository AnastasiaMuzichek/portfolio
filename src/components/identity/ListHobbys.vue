<script setup lang="ts">
import imageArt from '../../assets/images/hobby/art.png';
import imageFlat from '../../assets/images/hobby/flat.png';
import imageBook from '../../assets/images/hobby/book.png';
import imageFace from '../../assets/images/hobby/face.png';
import imageGamer from '../../assets/images/hobby/gamer.png';
import imageKinitting from '../../assets/images/hobby/kinitting.png';
import imageMusic from '../../assets/images/hobby/music.png';
import imagePlayer from '../../assets/images/hobby/player.png';
import { Row } from 'ant-design-vue';

const hobbysList = [
    {
        image: imageArt,
        name: 'рисование',
        description: 'творческая само-реализация, особенно нравится скетчи',
    },
    {
        image: imageFlat,
        name: 'прогулки',
        description: 'отдых на свежем воздухе',
    },
    {
        image: imageBook,
        name: 'чтение',
        description: 'расширят кругозор',
    },
    {
        image: imageKinitting,
        name: 'вязание',
        description: 'уютное рукоделие = спокойствие и уникальные вещи',
    },
    {
        image: imagePlayer,
        name: 'баскетбол',
        description: 'командный спорт и чувство драйва',
    },
    {
        image: imageMusic,
        name: 'музыка',
        description: 'помогает мне расслабиться или зарядиться энергией',
    },
    {
        image: imageFace,
        name: 'аниме',
        description:
            ' ценю за погружения в уникальные истории и ярких персонажей ',
    },
    {
        image: imageGamer,
        name: 'гейминг',
        description: 'люблю за возможность попасть в виртуальные приключения',
    },
];
</script>

<template>
    <Row justify="space-between" style="padding-top: 10px">
        <div v-for="hobby in hobbysList" class="hobby" :key="hobby.name">
            <div class="hobby-img">
                <img class="imageH" :src="hobby.image" />
                <span class="tooltiptext">{{ hobby.description }}</span>
            </div>

            <h3 class="hobby-title font-nea">
                {{ hobby.name }}
            </h3>
        </div>
    </Row>
</template>

<style scoped>
.hobby {
    display: inline-block;
    padding: 10px;
    padding-bottom: 5px;
}

.hobby-img {
    height: 5em;
    width: 5em;
    border: 0;
    border-radius: 50%;
    border: 3px solid rgb(14, 19, 90, 0.4);
    /* box-shadow: 4px 4px 8px rgba(14, 19, 90, 0.4); */
    display: flex;
    justify-content: center;
    align-items: center;
    transition: 0.2s linear;
    cursor: pointer;
    background-color: rgb(91, 91, 211);
}

.hobby-img .tooltiptext {
    visibility: hidden;
    position: absolute;
    background-color: rgba(91, 91, 211, 0.9);
    color: white;
    text-align: center;
    padding: 5px;
    border-radius: 6px;
    border: 2px solid rgba(14, 19, 90, 0.9);
    bottom: 100%;
    left: 50%;
    transform: translateX(-50%);
    margin-bottom: 10px;
    width: 90px;
    font-size: 12.5px;
}
.hobby-img:hover .tooltiptext {
    visibility: visible;
}

.hobby-title {
    margin: 0px;
    text-align: center;
}

.imageH {
    height: 4.5em;
}

.hobby-img:hover {
    box-shadow:
        0 0 0 2px white,
        0 0 0 4px #0e0750;
    transform: translate(0);
}
</style>
