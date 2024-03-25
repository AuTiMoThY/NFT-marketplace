<script setup>
import CollectionCard from '../components/CollectionCard.vue';


import { ref } from 'vue';

const collectionData = ref([
    {
        primaryPhoto: new URL('../assets/images/Trending-1-1.jpg', import.meta.url).href,
        secondaryPhoto: [
            new URL('../assets/images/Trending-1-2.jpg', import.meta.url).href,
            new URL('../assets/images/Trending-1-3.jpg', import.meta.url).href,
        ],
        numberNFT: '1025+',
        name: 'DSGN Animals',
        artistName: 'MrFox',
        artistImg: new URL('../assets/images/MrFox-small.jpg', import.meta.url).href,
    },
    {
        primaryPhoto: new URL('../assets/images/Trending-2-1.jpg', import.meta.url).href,
        secondaryPhoto: [
            new URL('../assets/images/Trending-2-2.jpg', import.meta.url).href,
            new URL('../assets/images/Trending-2-3.jpg', import.meta.url).href,
        ],
        numberNFT: '1025+',
        name: 'Magic Mushrooms',
        artistName: 'Shroomie',
        artistImg: new URL('../assets/images/Shroomie-small.jpg', import.meta.url).href,
    },
    {
        primaryPhoto: new URL('../assets/images/Trending-3-1.jpg', import.meta.url).href,
        secondaryPhoto: [
            new URL('../assets/images/Trending-3-2.jpg', import.meta.url).href,
            new URL('../assets/images/Trending-3-3.jpg', import.meta.url).href,
        ],
        numberNFT: '1025+',
        name: 'Disco Machines',
        artistName: 'BeKind2Robots',
        artistImg: new URL('../assets/images/BeKind2Robots-small.jpg', import.meta.url).href,
    },
]);

</script>


<template>
    <section class="page_section-trending">
        <div class="container">
            <div class="page_section-headline">
                <h2 class="heading">Trending Collection</h2>
                <p class="subhead">Checkout our weekly updated trending collection.</p>
            </div>
            <div class="page_section-content">
                <CollectionCard v-for="(item, index) in collectionData" :key="index" :primaryPhoto="item.primaryPhoto"
                    :secondaryPhoto="item.secondaryPhoto" :numberNFT="item.numberNFT" :name="item.name"
                    :artistName="item.artistName" :artistImg="item.artistImg"></CollectionCard>
            </div>
        </div>
    </section>
</template>