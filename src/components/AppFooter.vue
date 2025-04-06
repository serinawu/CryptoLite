<template>
    <footer>
        <div>
            <div class="aboutUs">
                <div class="logo">
                    <div class="brand-logo"></div>
                    <p class="brand-name">CryptoLite</p>
                </div>
                <p class="">Secure. Adaptive. Decentralized. <br/>The future of personal finance, today</p>
                <ul class="social-media">
                    <li><a><Icon icon="mdi:instagram" /></a></li>
                    <li><a><Icon icon="ri:pinterest-line" /></a></li>
                    <li><a><Icon icon="mingcute:threads-line"/></a></li>
                    <li><a><Icon icon="uil:linkedin"/></a></li>
                </ul>
            </div>
            <nav>
                <ul>
                    <h5>About Us</h5>
                    <li><a href="">Careers</a></li>
                    <li><a href="">Blog</a></li>
                    <li><a href="">Terms & Conditions</a></li>
                    <li><a href="">Privacy Policy</a></li>
                </ul>
                <ul>
                    <h5>Product</h5>
                    <li><a href="">Features</a></li>
                    <li><a href="">Wallet</a></li>
                    <li><a href="">Price Simulator</a></li>
                    <li><a href="">Daily Draw</a></li>
                    <li><a href="">Credit Card Designer</a></li>
                </ul>
                <ul>
                    <h5>Support</h5>
                    <li><a href="">Help Center</a></li>
                    <li><a href="">FAQ</a></li>
                    <li><a href="">Contact Us</a></li>
                    <li><a href="">Download App</a></li>
                    <li><a href="">Feedback</a></li>
                </ul>
            </nav>
        </div>
        <div class="copyRight">
            <p>&copy; 2022 CryptoLite. All rights reserved.</p>
        </div>
    </footer>
</template>
<script setup>
import { Icon } from '@iconify/vue';
</script>
<style lang="scss" scoped>
    footer {
        width: 100%;
        background: $bg-dark;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        &>div {
            width: flex;
            display: flex;
            justify-content: space-between;

            &:first-child {
                padding: $spacing-lg;
            }

            &.copyRight {
                padding: $spacing-md;
                border-top: 1px solid $color-grey;

                p {
                    color: $color-grey;
                    margin: auto;
                }
            }
        }

        .aboutUs {

            &>p {
                font-size: 1rem;
                color: $color-grey;
                margin-bottom: $spacing-md;
            }

            .social-media {
                display: flex;
                align-items: center;

                li {
                    width: 40px;
                    height: 40px;
                    margin-right: $spacing-md;
                    overflow: hidden;
                    cursor: pointer;

                    &:last-child {
                        margin-right: 0;
                    }
                    
                    a {
                        width: 100%;
                        height: 100%;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        border-radius: 50%;
                        background: white;
                        color: $color-secondary;
                        transition: all 0.3s;

                        i {
                            font-size: 1rem;
                        }
                    }

                    &:hover{

                        a {
                            background: $color-primary;
                            scale: 1.1;
                        }
                    }
                }
            }
        }

        nav {
            display: flex;
            justify-content: space-between;
            width: 60%;

            ul {
                display: flex;
                flex-direction: column;
                align-items: flex-start;
                margin-right: $spacing-lg;

                h5 {
                    font-size: 1.5rem;
                    color: white;
                    margin-bottom: $spacing-md;
                }

                li {
                    font-size: 1rem;
                    color: $color-grey;
                    margin-bottom: $spacing-sm;

                    a {
                        text-decoration: none;
                        color: $color-grey;
                        transition: all 0.3s;

                        &:hover {
                            color: white;
                        }
                    }
                }
            }
        }
    }
</style>