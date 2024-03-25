<script setup>
import Artist from '../components/Artist.vue';

defineProps({
    primaryPhoto: String,
    secondaryPhoto: Array,
    numberNFT: String,
    name: String,
    artistName: String,
    artistImg: String,
});
</script>

<template>
    <div class="collection_card">
        <div class="collection_card-hd">
            <div class="primary_photo">
                <div class="img_wrap">
                    <img :src="primaryPhoto" alt="" class="img">
                </div>
            </div>
            <div class="secondary_photo">
                <div class="secondary_photo-item">
                    <div class="img_wrap">
                        <img :src="secondaryPhoto[0]" alt="" class="img">
                    </div>
                </div>
                <div class="secondary_photo-item">
                    <div class="img_wrap">
                        <img :src="secondaryPhoto[1]" alt="" class="img">
                    </div>
                </div>
                <div class="secondary_photo-item">
                    <div class="number">{{ numberNFT }}</div>
                </div>
            </div>
        </div>
        <div class="collection_card-bd">
            <div class="name">{{ name }}</div>
            <Artist :src="artistImg" :name="artistName"></Artist>
        </div>
    </div>
</template>