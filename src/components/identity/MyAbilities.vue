<script setup lang="ts">
import { LayoutContent, Tag } from 'ant-design-vue';
import { Chart as ChartJS, ArcElement, Tooltip } from 'chart.js';
import { Pie } from 'vue-chartjs';
import imageEfficiency from '../../assets/images/abilities/efficiency.png';
import imageCommunication from '../../assets/images/abilities/communication_skills.png';
import imageInterpersonal from '../../assets/images/abilities/interpersonal_communication_skills.png';
import imageLearning from '../../assets/images/abilities/learning_ability.png';
import imageOrganizational from '../../assets/images/abilities/organizational_skills.png';
import imagePrecision from '../../assets/images/abilities/precision_and_attention_detail.png';
import imageStress from '../../assets/images/abilities/stress _esistance.png';
import type { ChartMeta, ChartOptions, Plugin } from 'chart.js';

const images: CanvasImageSource[] = [];

const data = {
    labels: [
        'РАБОТОСПОСОБНОСТЬ',
        'КОММУНИКАБЕЛЬНОСТЬ',
        'ОБУЧАЕМОСТЬ',
        'НАВЫКИ МЕЖЛИЧНОСТНОГО ОБЩЕНИЯ',
        'ОРГАНИЗАЦИОННЫЕ НАВЫКИ',
        'ТОЧНОСТЬ И ВНИМАТЕЛЬНОСТЬ К ДЕТАЛЯМ',
        'СТРЕССОУСТОЙЧИВОСТЬ',
    ],
    datasets: [
        {
            backgroundColor: [
                'rgb(45, 45, 209)',
                'rgb(14, 45, 90)',
                'rgb(81, 38, 81)',
                'rgb(24, 24, 28)',
                'rgb(129, 129, 197)',
                'rgb(10, 10, 57)',
                'rgb(85, 19, 200)',
            ],
            data: [40, 40, 40, 40, 40, 40, 40],
        },
    ],
};

const options: ChartOptions<'pie'> = {
    responsive: true,
    maintainAspectRatio: false,
    elements: {
        arc: {
            hoverOffset: 60,
            offset: 8,
        },
    },
    layout: {
        padding: 18,
    },
    plugins: {
        tooltip: {
            titleColor: 'rgb(255, 255, 255)',
            titleMarginBottom: 0,
            backgroundColor: 'rgb(91, 91, 211, 0.8)',
            borderColor: 'rgb(14, 19, 90, 0.8)',
            borderWidth: 2,

            callbacks: {
                label: () => '',
            },
        },
    },
};

ChartJS.register(ArcElement, Tooltip);

const plugin: Plugin<'pie'> = {
    afterDatasetDraw(
        { ctx, data },
        args: { index: number; meta: ChartMeta<'pie', ArcElement> },
    ) {
        const arcs = args.meta.data;
        const values = data.datasets[0]?.data ?? [];

        for (let i = 0; i < values.length; i++) {
            const arc = arcs[i];
            const image = images[i];

            if (!arc || !image) {
                continue;
            }

            const { x, y } = arc.getCenterPoint(true);

            ctx.drawImage(image, x - 25, y - 25, 50, 50);
        }
    },
    id: 'icon-plugin',
};

function prepareImages() {
    [
        imageEfficiency,
        imageCommunication,
        imageLearning,
        imageInterpersonal,
        imageOrganizational,
        imagePrecision,
        imageStress,
    ].forEach((item) => {
        const image = new Image();
        image.src = item;
        images.push(image);
    });
}

prepareImages();
</script>

<template>
    <LayoutContent class="abilities">
        <Tag color="rgb(91, 91, 211)" class="font-nea text-abilities"
            >Мои навыки</Tag
        >
        <div class="div-pie">
            <Pie
                :data="data"
                :options="options"
                style="margin-top: 20px"
                :plugins="[plugin]"
            ></Pie>
        </div>
    </LayoutContent>
</template>

<style scoped>
.abilities {
    background-color: aliceblue;
    padding-left: 16px;
    border: 2px rgb(91, 91, 211);
    border-style: solid none none none;
    position: relative;
}

.text-abilities {
    font-size: 20px;
    position: absolute;
    top: -10px;
    left: 16px;
    height: 20px;
    width: 150px;
    text-align: center;
}

.div-pie {
    height: 400px;
}
</style>
