<template>
    <container-box title="相关外链" subtitle="友情链接">
        <a-typography>
            <a-typography-title underline v-for="(el, index) in lineData" :heading="index + 1" :key="el">
                <component :is="el.icon" />
                <a :href="el.href" target="blank">{{ el.label }}</a>
            </a-typography-title>
        </a-typography>
    </container-box>
</template>

<script setup>
import { reactive } from "@vue/reactivity";

let lineData = reactive([
    {
        label: "Github地址",
        href: "https://github.com/poboll/ez-admin",
        icon: "icon-github",
    },
    {
        label: "ArcoDesign",
        href: "https://arco.design/vue/docs/start",
        icon: "icon-link",
    },
]);
</script>

<style scoped>
a {
    text-decoration: none;
    color: #000;
    margin-left: 16px;
}
</style>
