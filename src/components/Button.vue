<script setup>
defineProps({
    iconHtml: Object,
    txt: String,
    btnClass: String,
    link: String,
});
</script>

<template>
    <a :href="link" :class="['nft_btn', btnClass]">
        <component :is="iconHtml" class="icon"></component>
        <span class="txt">{{ txt }}</span>
    </a>
</template>