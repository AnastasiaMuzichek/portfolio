<script setup lang="ts"></script>

<template>
    <div class="myphoto">
        <img src="../assets/images/photo.jpg" />
    </div>
</template>

<style scoped>
.myphoto {
    width: 150px;
    display: flex;
    justify-content: center;
}

img {
    height: 150px;
    border-radius: 50%;
    border: 2px solid rgb(91, 91, 211);
    box-shadow: 4px 4px 8px rgba(14, 19, 90, 0.4);
    transition: 0.2s linear;
    cursor: pointer;
}
img:hover {
    box-shadow:
        0 0 0 3px white,
        0 0 0 7px #0e0750;
}
</style>
