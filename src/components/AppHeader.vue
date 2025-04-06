<template>
    <header>
        <div class="logo">
            <div class="brand-logo"></div>
            <p class="brand-name">CryptoLite</p>
        </div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Features</a></li>
                <li><a href="#">Product</a></li>
                <li><a href="#">App</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
        <div class="btnGroup">
            <button class="loginBtn">Log in</button>
            <button class="SignupBtn">Sign up</button>
        </div>
    </header>
</template>
<script setup>
</script>
<style lang="scss" scoped>
header {
    width: 100%;
    height: 80px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 $spacing-md;

    &::before {
        content: "";
        width: 100%;
        height: 100%;
        position: absolute;
        inset: 0;
        z-index: -1;
        backdrop-filter: blur(10px); 
        background: #00000054;
        -webkit-backdrop-filter: blur(10px);
    }

    nav {

        ul {
            display: flex;
            align-items: center;
            
            li {
                margin-right: $spacing-md;

                &:last-child {
                    margin-right: 0;
                }

                a {
                    text-decoration: none;
                    transition: all 0.3s;

                    &:hover {
                        color: $primary-color;
                    }
                }
            }
        }
    }

    .btnGroup {
        display: flex;
        align-items: center;

        button {
            padding: 12px 24px;
            border-radius: 99px;
            font-weight: bold;
            transition: all 0.3s;
        }

        .loginBtn {
            border: 1px solid $primary-color;
            background: transparent;
            color: $primary-color;
            margin-right: $spacing-md;
        }

        .SignupBtn {
            background: white;
            color: $color-secondary;
        }
    }
}
</style>