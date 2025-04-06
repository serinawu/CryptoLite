<template>
    <section class="hero">
        <div class="hero-body">
            <div class="hero__content">
                <h1 class="brand">
                    {{ title }}
                </h1>
                <h2 class="subtitle">
                    {{ subtitle }}
                </h2>
                <button @click="handleClick" class="bonusBtn">
                    <p>Claim your welcome bonus</p>
                    <span><Icon icon="maki:arrow" class="icon"/></span>
                </button>
            </div>
            <div class="hero_right">
                <div class="hero__image">
                    <img class="card" src="@/assets/images/CartGradient .png" alt="credit card" />
                    <img class="mock" src="../assets/images/iphone14pro.png" alt="Credit Card App" />
                </div>
                <ul class="result">
                    <li>
                        <p class="number">3y+</p>
                        <p class="info">In Service</p>
                    </li>
                    <li>
                        <p class="number">10+</p>
                        <p class="info">Global Partners</p>
                    </li>
                    <li>
                        <p class="number">10.2K+</p>
                        <p class="info">Active Users</p>
                    </li>
                </ul>
            </div>
        </div>
        <button class="goBtn"><Icon icon="line-md:arrow-down"/></button>
    </section>
</template>
<script setup>
    import {ref} from 'vue';
    import { Icon } from '@iconify/vue';
    const title = ref('CryptoLite')
    const subtitle = ref('Your smart companion for crypto investment.')
</script>
<style scoped lang="scss">
    .hero {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: $spacing-lg;
        background: linear-gradient(135deg, #0d0d0d, #111111);
        min-height: 100vh;
        position: relative;

        .goBtn {
            position: absolute;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50px;
            font-size: 1.2rem;
            // animation: float 3s ease-in-out infinite;
            cursor: pointer;
        }

        &-body {
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: space-around;
            overflow: hidden;
        }

        &__content {
       
            h1 {
                font-size: 5rem;
                color: $primary-color;
                margin-bottom: $spacing-md;
            }

            h2 {
                width: 60%;
                font-size: 3rem;
                color: white;
                line-height: normal;
            }

            button {
                display: flex;
                align-items: center;
                font-weight: bold;
                margin-top: $spacing-lg;
                transition: all 0.3s;

                &.bonusBtn {
                    padding: 10px 10px 10px 32px;
                    border-radius: 99px;
                    font-size: 1rem;
                    transition: all 0.3s;
                    
                    &:hover {
                        background: lighten($color-primary, 10%);
                        
                        span {
                            svg {
                                transform: rotate(45deg)scale(1.3);
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
                    margin-left: $spacing-sm;

                    icon {
                        font-size: 6rem;
                        color: $color-secondary;
                    }
                }
                
            }
        }

        &_right {

            .result {
                display: flex;
                justify-content: space-around;
                width: 103%;
                margin-top: 400px;

                li {
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    padding: $spacing-md;
                    border-radius: 12px;
                    color: white;
                    font-size: 1.5rem;
                    font-weight: bold;
                    transition: all 0.3s;

                    .number {
                        font-size: 2.5rem;
                        margin-bottom: $spacing-xs;
                    }

                    .info {
                        font-size: 1rem;
                        font-weight: normal;
                        color: $color-grey;
                    }
                }
            }
        }

        &__image {
            position: relative;
            
            img {
                width: 350px;
                // filter: drop-shadow(0 0 15px $color-primary);
                margin: 0 auto;
                
                &.card {
                    position: absolute;
                    top: 100px;
                    left: -76px;
                    animation: float 3s ease-in-out infinite;
                    z-index: 3;
                }

                &.mock {
                    width: 450px;
                    position: absolute;
                    top: -49px;
                    left: -436px;
                    transform: skewX(13deg);
                }
            }
        }
    }
    
    @keyframes float {
        0%, 100% {
            transform: translateY(0px)skewX(13deg);
        }
        50% {
            transform: translateY(-10px)skewX(13deg);
        }
    }
</style>