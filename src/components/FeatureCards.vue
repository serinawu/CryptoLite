<template>
    <section class="features">
        <div class="customer">
            <div class="company" v-for="(cs, index) in customer" :key="index">
                <img :src="cs.logo" alt="company logo" />
            </div>
        </div>
        <h1>What do we offer?</h1>
        <h4>Since 2013 we've guided millions of global<br/>users on their digital assets journey!</h4>
        <div class="feature">
            <div class="feature_card" v-for="(item, index) in features" :key="index">
                <Icon :icon="item.icon" class="icon"></Icon>
                <h3>{{ item.title }}</h3>
                <p>{{ item.desc }}</p>
            </div>
        </div>
    </section>
</template>
<script setup>
import { Icon } from '@iconify/vue';
const customer = [
    {
        logo: 'src/assets/images/petal.png',
    },
    {
        logo: 'src/assets/images/Rakuten.png',
    },
    {
        logo:'src/assets/images/Vice.png',
    },
    {
        logo:'src/assets/images/Dell.png',
    },
    {
        logo:'src/assets/images/Upwork.png',
    }
]

const features = [
    {
        icon: 'mdi:chart-line',
        title: 'Real-time Crypto Prices',
        desc: 'Track major cryptocurrencies with live market data.',
    },
    {
        icon: 'mdi:lightbulb-on-outline',
        title: 'Smart Investment Insights',
        desc: 'Get guidance on when to hold, sell or buy with trend-based analysis.',
    },
    {
        icon: 'mdi:gift-outline',
        title: 'Daily Reward Draws',
        desc: 'Earn chances to win rewards by joining daily investment activities.',
    },
    {
        icon: 'material-symbols:lock',
        title: 'Secure Transactions',
        desc: 'Enjoy peace of mind with our secure and encrypted transactions.',
    }
]
</script>
<style scope lang="scss">
    .features {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding:$spacing-lg 0;
        background: $bg-light;

        .customer {
            width: 100%;
            display: flex;
            align-items: center;
            margin-bottom: $spacing-lg;
            overflow: hidden;
            
            .company {
                width: calc(100% / 5);
                height: 100px;
                display: flex;
                align-items: center;
                justify-content: center;
                background: white;
                border-radius: 30px;

                img {
                    width: 150px;
                    height: auto;
                    filter: grayscale(100%) brightness(2);
                    opacity: 0.8;
                }
            }
        }

        h1 {
            font-size: 3.5rem;
            color: $color-secondary;
            text-align: center;
            margin: $spacing-lg 0 $spacing-xs 0;
        }

        h4 {
            font-size: 1.2rem;
            color: $color-grey;
            text-align: center;
            margin-bottom: $spacing-lg;
        }

        .feature {
            display: flex;
            align-content: center;
            justify-content: space-around;
            padding: 0 $spacing-lg;  
            margin-top: $spacing-lg;

            &_card {
                width: calc(95% / 4);
                height: 350px;
                background: white;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                border-radius: 12px;
                padding: spacing-md;
                text-align: center;
                transition: transform 0.3s ease, box-shadow 0.3s ease; 

                &:hover {
                    transform: translateY(-10px);
                    // box-shadow: $card-shadow-hover;
                }

                .icon {
                    font-size: 5rem;
                    color: $primary-color;
                    margin-bottom: $spacing-lg;
                }

                h3 {
                    font-size: 1.3rem;
                    color: $color-secondary;
                    font-weight: bold;
                    margin-bottom: $spacing-lg 0 $spacing-sm 0;
                }

                p {
                    width: 90%;
                    font-size: 1rem;
                    color: $color-grey;
                    font-weight: normal;
                    margin-bottom: $spacing-sm;
                }
            }
        }
    }
</style>
