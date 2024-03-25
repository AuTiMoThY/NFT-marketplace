<script setup>
defineProps({
    src: String,
    name: String,

});
</script>
<template>
    <div class="artist">
        <div class="img"><img :src="src" alt="{{name}}"></div>
        <div class="name">{{ name }}</div>
    </div>
</template>