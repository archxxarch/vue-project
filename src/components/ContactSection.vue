<script setup>
import { contactText } from "@/constants/index"
</script>

<template>
    <section id="contact">
        <div class="contact__inner">
            <h2 class="contact__title">Contact</h2>

            <div class="contact__text">
                <div class="text" v-for="(contact, key) in contactText" :key="key">
                    <div>
                        <a href="contact.link">{{ contact.title }}
                        </a>
                    </div>
                </div>
            </div>

            <div class="contact__lines" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>

        </div>
    </section>
</template>

<style lang="scss">
#contact {
    height: 100vh;
}

.contact__inner {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    flex-direction: column;
    padding: 1vw;
}

.contact__title {
    font-size: 9.9vw;
    text-transform: uppercase;
    font-weight: 800;
    font-family: var(--mainPop-font);
    line-height: 0.95;
    letter-spacing: -0.3vw;
    color: var(--mainSub-color);
}

.contact__text {
    width: 100%;
    height: 40vh;
    color: var(--mainBg-color);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    position: relative;
    font-family: var(--mainPop-font);
    background-color: var(--mainSub-color);
}

.contact__text .text {
    font-size: 2vw;
    line-height: 1;
    text-align: center;
    position: relative;
    z-index: 100;
    transition: all 0.3s;
    cursor: all-scroll;
    font-family: var(--mainPop-font);
}

.contact__lines {
    display: block;
    width: 100%;
}

.contact__lines .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: var(--subBg300);
    margin-bottom: 0.5vw;
}

.contact__lines .line:nth-child(1) {
    height: 7px;
}

.contact__lines .line:nth-child(2) {
    height: 6px;
}

.contact__lines .line:nth-child(3) {
    height: 5px;
}

.contact__lines .line:nth-child(4) {
    height: 4px;
}

.contact__lines .line:nth-child(5) {
    height: 3px;
}

.contact__lines .line:nth-child(6) {
    height: 2px;
}

.contact__lines .line:nth-child(7) {
    height: 1px;
}

.contact__lines.bottom {
    display: none;
}

.contact__lines.bottom .line:nth-child(1) {
    height: 7px;
}

.contact__lines.bottom .line:nth-child(2) {
    height: 6px;
}

.contact__lines.bottom .line:nth-child(3) {
    height: 5px;
}

.contact__lines.bottom .line:nth-child(4) {
    height: 4px;
}

.contact__lines.bottom .line:nth-child(5) {
    height: 3px;
}

.contact__lines.bottom .line:nth-child(6) {
    height: 2px;
}

.contact__lines.bottom .line:nth-child(7) {
    height: 1px;
}

@media (max-width: 800px) {
    .contact__inner {
        align-items: center;
        justify-content: center;
    }

    .contact__lines.bottom {
        display: block;
    }

    .contact__title {
        display: none;
    }

    .contact__text .text {
        font-size: 30px;
    }

    .contact__text .text>div:nth-child(2) {
        filter: brightness(0.5);
    }


    .contact__text .img::after {
        opacity: 0.3;
    }

}
</style>
