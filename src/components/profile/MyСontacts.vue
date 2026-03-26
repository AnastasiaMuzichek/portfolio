<script setup lang="ts">
import { Flex, LayoutSider, Space, Tag } from 'ant-design-vue';
import {
    GithubFilled,
    WhatsAppOutlined,
    MailOutlined,
} from '@ant-design/icons-vue';
</script>

<template>
    <LayoutSider class="frame">
        <Tag color="rgb(91, 91, 211)" class="font-nea text-contact">
            Контакты
        </Tag>
        <Flex vertical gap="10">
            <Space align="middle">
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
                >
                    GitHub
                </a>
            </Space>
            <Space align="middle">
                <img
                    class="icon"
                    src="../../assets/images/telegram.png"
                    style="height: 20px"
                />
                <a href="https://telegram.me/lady_anger" target="_blank">
                    @lady_anger
                </a>
            </Space>
            <Space align="middle">
                <img
                    class="icon"
                    src="../../assets/images/hh_logo.png"
                    style="height: 20px"
                />
                <a
                    href="https://samara.hh.ru/resume/3282f445ff08f2b2cc0039ed1f354538753358"
                    target="_blank"
                >
                    hh-резюме
                </a>
            </Space>
        </Flex>
    </LayoutSider>
</template>

<style scoped>
.ant-layout .ant-layout-sider {
    background-color: inherit;
    padding: 16px;
    padding-top: 36px;
}

.text-contact {
    font-size: 20px;
    position: absolute;
    top: -10px;
    left: 45px;
    height: 20px;
    width: 100px;
    text-align: center;
}

.frame {
    border: 2px solid rgb(91, 91, 211);
    border-radius: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 220px;
    margin-top: 15px;
}

.icon {
    font-size: 20px;
    color: rgb(91, 91, 211);
}
</style>
