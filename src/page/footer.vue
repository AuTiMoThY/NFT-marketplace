<script setup>
import DiscordLogo from '../components/icons/DiscordLogo.vue';
import InstagramLogo from '../components/icons/InstagramLogo.vue';
import TwitterLogo from '../components/icons/TwitterLogo.vue';
import YoutubeLogo from '../components/icons/YoutubeLogo.vue';
import EnvelopeSimple from '../components/icons/EnvelopeSimple.vue';
</script>
<template>
    <footer class="site_footer">
        <div class="container row-3-parts">
            <div class="info">
                <div class="logo">
                    <img alt="NFT Marketplace logo" class="logo" src="../assets/logo.svg">
                </div>
                <div class="additional_info">
                    <p class="txt">NFT marketplace UI created with Anima for Figma.</p>
                    <div class="community_info">

                        <div class="txt">Join our community</div>
                        <div class="icons">
                            <a href="javascript:;" class="icon">
                                <DiscordLogo></DiscordLogo>
                            </a>
                            <a href="javascript:;" class="icon">
                                <InstagramLogo></InstagramLogo>
                            </a>
                            <a href="javascript:;" class="icon">
                                <TwitterLogo></TwitterLogo>
                            </a>
                            <a href="javascript:;" class="icon">
                                <YoutubeLogo></YoutubeLogo>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            <div class="explore">
                <b class="title">Explore</b>
                <ul class="explore-list">
                    <li class="explore-item"><a href="" class="link">Marketplace</a></li>
                    <li class="explore-item"><a href="" class="link">Rankings</a></li>
                    <li class="explore-item"><a href="" class="link">Connect a wallet</a></li>
                </ul>
            </div>
            <div class="subscribe">
                <b class="title">Join our weekly digest</b>
                <div class="subscribe-frm">
                    <p class="txt">Get exclusive promotions & updates straight to your inbox.</p>
                    <div class="subscribe-field">
                        <input type="text" class="subscribe-field-input" placeholder="Enter your email here">
                        <button class="subscribe-field-btn">
                            <div class="icon">
                                <EnvelopeSimple></EnvelopeSimple>
                            </div>
                            <span class="txt">Subscribe</span>
                        </button>
                    </div>
                </div>
            </div>
        </div>
        <div class="container ">
            <div class="copyright">
                Ⓒ NFT Market. Use this template freely.
            </div>
        </div>
    </footer>
</template>