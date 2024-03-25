<script setup>
import Btn from '../components/Button.vue';
import UserIcon from '../components/icons/icon-User.vue';
import CloseIcon from '../components/icons/icon-close.vue';
import BurgerMenu from '../components/icons/BurgerMenu.vue';

import { ref, watch } from 'vue';
const isMenuOpen = ref(false);
watch(isMenuOpen, (newValue) => {
    if (newValue) {
        document.querySelector("body").classList.add("js-open-mobile-menu");
    } else {
        document.querySelector("body").classList.remove("js-open-mobile-menu");
    }
});
const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
};

</script>

<template>
    <header class="site_header">
        <div class="container">
            <a href="./" class="logo">
                <img alt="NFT Marketplace logo" class="logo" src="../assets/logo.svg">
            </a>
            <div class="nav">
                <div class="nav-close" @click="toggleMenu()">
                    <CloseIcon></CloseIcon>
                </div>
                <ul class="nav-list">
                    <li class="nav-item">
                        <a href="" class="link">Marketplace</a>
                    </li>
                    <li class="nav-item">
                        <a href="" class="link">Rankings</a>
                    </li>
                    <li class="nav-item">
                        <a href="" class="link">Connect a wallet</a>
                    </li>
                </ul>
                <div class="nav-quick">
                    <Btn :iconHtml="UserIcon" txt="Sign Up" link="./"></Btn>
                </div>
            </div>
            <div class="burger_menu">
                <BurgerMenu @click="toggleMenu()"></BurgerMenu>
            </div>
        </div>
    </header>
</template>