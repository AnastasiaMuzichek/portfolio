<script setup lang="ts">
import {
    TypographyParagraph,
    Tag,
    Collapse,
    CollapsePanel,
    List,
} from 'ant-design-vue';

defineProps({
    date: String,
    company: String,
    description: String,
    descriptions: List,
});
</script>

<template>
    <div class="card-work">
        <Tag color="rgb(91, 91, 211)" class="font-nea data-work">{{
            date
        }}</Tag>
        <Collapse>
            <CollapsePanel :header="company" class="font-nea">
                <TypographyParagraph>
                    <ul
                        v-for="st in descriptions"
                        style="list-style-type: disc"
                    >
                        <li class="list-work">{{ st }}</li>
                    </ul>
                </TypographyParagraph>
            </CollapsePanel>
        </Collapse>
    </div>
</template>

<style scoped>
.ant-card .ant-card-body {
    padding: 0px;
}

h3.ant-typography {
    margin: 0;
    padding-bottom: 10px;
}

div.ant-typography {
    margin: 0;
}

.card-work {
    display: flex;
}

.data-work {
    font-size: 20px;
    height: 30px;
    display: flex;
    align-items: center;
}

.ant-collapse {
    flex: 1;
}

.ant-collapse,
.ant-collapse > .ant-collapse-item {
    border-color: rgb(91, 91, 211);
    border-width: 2px;
}

:deep(.ant-collapse-item > .ant-collapse-header) {
    padding: 12px;
}
:deep(.ant-collapse-item > .ant-collapse-header > .ant-collapse-header-text) {
    font-size: 18px;
}

:deep(.ant-collapse-item > .ant-collapse-header > .ant-collapse-expand-icon) {
    height: 28px;
}

.list-work {
    font-size: 16px;
}
li::marker {
    color: rgb(91, 91, 211);
}
</style>
