<template>
    <section class="promo">
        <div class="promo_content">
            <div class="text-left">
                <h2>Find the <br />Perfect Credit Card</h2>
                <p>Design your card, track your spending, and get rewarded — all in one app.</p>
                <div class="store-buttons">
                    <button class="appStoreBtn"></button>
                    <button class="googlePlayBtn"></button>
                </div>
            </div>
            <div class="mockup-center">
            <img src="../assets/images/iphone14pro.png" alt="Credit Card App" />
            </div>
            <div class="cta-right">
            <h3>Easy Way to <br /><span>Manage your Finance</span></h3>
            <button @click="handleClick" class="quickSignUpBtn">
                <p>Sign UP Now!!</p>
                <span><Icon icon="maki:arrow" class="icon"/></span>
            </button>
            </div>
        </div>
    </section>
</template>
<script setup>
import { Icon } from '@iconify/vue';
</script>
<style lang="scss" scoped>
    .promo {
        display: flex;
        align-items: center;
        justify-content: space-between;
        background: $bg-light;

        &_content {
            width: 95%;
            height: 90%;
            display: flex;
            justify-content: space-between;
            background: $bg-dark;
            border-radius: 30px;
            margin: auto;            

            .text-left {
                width: 30%;
                display: flex;
                flex-direction: column;
                justify-content: center;
                padding: $spacing-lg; 

                h2 {
                    font-size: 3rem;
                    line-height: 3rem;
                    margin-bottom: $spacing-md;
                }
                
                .store-buttons {
                    display: flex;
                    align-items: center;
                    margin-top: $spacing-lg;

                    button {
                        width: 150px;
                        height: 50px;
                        border-radius: 8px;
                        overflow: hidden;
                        transition: all 0.3s;

                        &:hover {
                            transform: scale(1.05);
                        }

                        &.appStoreBtn {
                            background: url(../assets/images/appstore.svg) no-repeat;
                            background-size: 101%;
                            background-position: center;
                            margin-right: $spacing-md;
                        }

                        &.googlePlayBtn {
                            background: url(../assets/images/google-play-app-store-android.jpg) no-repeat;
                            background-size: 103%;
                            background-position: center;
                            filter:contrast(4);
                        }
                    }
                }
            }

            .mockup-center {
                width: 40%;
                padding: $spacing-lg;
                overflow: hidden;

                img {
                    width: 100%;
                    height: auto;
                }
            }

            .cta-right {
                width: 30%;
                padding: $spacing-lg;
                display: flex;
                flex-direction: column;
                justify-content: center;

                h3 {
                    font-size: 3rem;
                    line-height: 3rem;
                    margin-bottom: $spacing-md;

                    span {
                        color: $color-primary;
                    }
                }

                button {
                    display: flex;
                    align-items: center;
                    font-weight: bold;
                    margin-top: $spacing-lg;
                    transition: all 0.3s;

                        &.quickSignUpBtn {
                            width: fit-content;
                            padding: 10px 10px 10px 32px;
                            border-radius: 99px;
                            font-size: 1rem;
                            
                            &:hover {
                                span {
                                svg {
                                    transform: rotate(-45deg)scale(1.3);
                                }
                            }
                        }
                    }
                
                    p {
                        font-size: 1.19rem;
                    }

                    span {
                        width: 50px;
                        height: 50px;
                        background: $color-primary;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        border-radius: 50px;
                        margin-left: $spacing-md;

                        icon {
                            font-size: 6rem;
                            color: $color-secondary;
                        }
                    }
                }
            }
        }
    }
</style>