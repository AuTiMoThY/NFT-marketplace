<script setup>
import Btn from '../components/Button.vue';
import RocketIcon from '../components/icons/icon-RocketLaunch.vue';
import ArtistCard from '../components/ArtistCard.vue';


import { ref } from 'vue';

const artistList = [
    'Keepitreal',
    'DigiLab',
    'GravityOne',
    'Juanie',
    'BlueWhale',
    'MrFox',
    'Shroomie',
    'robotica',
    'RustyRobot',
    'Animakid',
    'Dotgu',
    'Ghiblier',
];
const artistData = ref(artistList.map(name => ({
    imgSrc: new URL(`../assets/images/${name.replace(/\s+/g, '')}.jpg`, import.meta.url).href,
    name: name,
    total: '34.53',
})));
</script>

<template>
    <section class="page_section-top_creators">
        <div class="container">
            <div class="page_section-headline">
                <div class="txts_group">
                    <h2 class="heading">Top creators</h2>
                    <p class="subhead">Checkout Top Rated Creators on the NFT Marketplace</p>
                </div>
                <Btn :iconHtml="RocketIcon" txt="View Rankings" link="./" btnClass="nft_btn-nobg"></Btn>
            </div>
            <div class="page_section-content">
                <ul class="artist-list">
                    <li class="artist-item" v-for="(item, index) in artistData" :key="index">
                        <ArtistCard :imgSrc="item.imgSrc" :name="item.name" :total="item.total"></ArtistCard>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>