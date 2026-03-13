<script setup lang="ts">
import {
    Card,
    TypographyParagraph,
    TypographyText,
    TypographyTitle,
} from 'ant-design-vue';

defineProps({
    date: String,
    company: String,
    description: String,
});
</script>

<template>
    <Card>
        <TypographyTitle :level="3">{{ company }}</TypographyTitle>
        <TypographyText>{{ date }}</TypographyText>
        <TypographyParagraph>{{ description }}</TypographyParagraph>
    </Card>
</template>

<style scoped>
.ant-card .ant-card-body {
    padding: 0px;
}
</style>
