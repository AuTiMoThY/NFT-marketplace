<script setup>
import Btn from '../components/Button.vue';
import UserIcon from '../components/icons/icon-User.vue';
</script>

<template>
    <header class="site_header">
        <div class="container">
            <a href="./" class="logo">
                <img alt="NFT Marketplace logo" class="logo" src="../assets/logo.svg">
            </a>
            <div class="nav">
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
        </div>
    </header>
</template>