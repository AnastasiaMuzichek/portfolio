<script setup lang="ts">
import { Flex, LayoutSider, Space, Tag } from 'ant-design-vue';
import {
    GithubFilled,
    WhatsAppOutlined,
    MailOutlined,
} from '@ant-design/icons-vue';
</script>

<template>
    <LayoutSider class="frame" style="background-color: aliceblue">
        <Tag color="rgb(91, 91, 211)" class="font-nea" style="font-size: 20px"
            >Контакты</Tag
        >
        <Flex vertical gap="10">
            <Space style="margin-top: 20px" align="middle">
                <WhatsAppOutlined class="icon"></WhatsAppOutlined>
                8-(927)-003-78-49
            </Space>
            <Space align="middle">
                <MailOutlined class="icon"></MailOutlined>

                <a href="mailto:nmuzychek@yandex.ru">nmuzychek@yandex.ru</a>
            </Space>
            <Space align="middle">
                <GithubFilled class="icon"></GithubFilled>
                <a
                    href="https://github.com/AnastasiaMuzichek"
                    target="_blank"
                    rel="noopener noreferrer"
                    >GitHub</a
                >
            </Space>
            <Space align="middle">
                <img
                    class="icon"
                    src="../../assets/images/telegram.png"
                    style="height: 20px"
                />
                <a href="https://telegram.me/lady_anger" target="_blank"
                    >@lady_anger</a
                >
            </Space>
        </Flex>
    </LayoutSider>
</template>

<style scoped>
.ant-layout .ant-layout-sider {
    background-color: antiquewhite;
    padding: 16px;
}

.ant-layout .ant-layout-content {
    padding: 16px;
}

.frame {
    background-color: aliceblue;
    border: 2px solid rgb(91, 91, 211);
    border-radius: 15%;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 195px;
}

.icon {
    font-size: 20px;
    color: rgb(91, 91, 211);
}
</style>
