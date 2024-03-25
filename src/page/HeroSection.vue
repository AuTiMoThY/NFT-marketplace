<script setup>
import Btn from '../components/Button.vue';
import Artist from '../components/Artist.vue';
import RocketIcon from '../components/icons/icon-RocketLaunch.vue';

import { ref } from 'vue';

const additional_info = ref([
    { label: 'Total Sale', number: '240k+' },
    { label: 'Auctions', number: '100k+' },
    { label: 'Artists', number: '240k+' }
]);
const HighlightArtistImg = new URL('../assets/images/Animakid-small.jpg', import.meta.url).href;
</script>

<template>
    <section class="page_section-hero">
        <div class="container">
            <!-- <div class="txts">
            </div> -->
            <div class="heading_group">
                <h1 class="title">Discover Digital Art & Collect NFTs</h1>
                <p class="txt">NFT marketplace UI created with Anima for Figma. Collect, buy and sell art from more than
                    20k NFT artists.</p>
            </div>
            <Btn :iconHtml="RocketIcon" txt="Get Started" link="javascript:;"></Btn>
            <div class="additional_info">
                <div class="additional_info-item" v-for="(item, index) in additional_info" :key="index">
                    <span class="number">{{ item.number }}</span>
                    <span class="label">{{ item.label }}</span>
                </div>
            </div>
            <div class="highlight_NFT">
                <div class="nft_card">
                    <div class="nft_card-img">
                        <img src="../assets/images/main-image.jpg" alt="">
                    </div>
                    <div class="nft_card-info">
                        <div class="name">Space Walking</div>
                        <Artist :src="HighlightArtistImg" name="Animakid"></Artist>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>