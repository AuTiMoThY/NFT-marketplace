<script setup>


defineProps({
    imgSrc: String,
    name: String,
    total: String
});
</script>
<template>
    <a class="artist_card" href="javascript:;">
        <div class="artist_card-avatar">
            <div class="img_wrap">
                <img :src="imgSrc" alt="">
            </div>
        </div>
        <div class="artist_card-info">
            <div class="name">{{ name }}</div>
            <div class="total">
                <span class="label">Total Sales:</span><span class="number"> {{ total }} ETH</span>
            </div>
        </div>
    </a>
</template>