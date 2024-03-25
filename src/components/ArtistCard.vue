<script setup>


defineProps({
    imgSrc: String,
    name: String,
    total: String
});
</script>
<template>
    <div class="artist_card">
        <div class="artist_card-avatar">
            <div class="img_wrap">
                <img :src="imgSrc" alt="">
            </div>
        </div>
        <div class="artist_card-info">
            <div class="name">{{ name }}</div>
            <div class="total">
                <span class="small">Total Sales:</span> {{ total }} ETH
            </div>
        </div>
    </div>
</template>