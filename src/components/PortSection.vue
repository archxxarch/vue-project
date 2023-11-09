<script setup>
import { portText } from "@/constants/index"
</script>


<template>
    <section id="port">
        <div class="port__inner">
            <div class="port__title">
                portfolio <em>3D 작업물</em>
            </div>
            <div class="port__wrap">
                <div :class="`port__item p${key + 1}`" v-for="(port, key) in portText" :key="key">
                    <span class="num">{{ port.num }}.</span>
                    <a href="#">
                        <img :src="port.img" :alt="port.name" />
                    </a>
                    <h3 class="title">{{ port.title }}</h3>
                    <p class="desc">{{ port.desc }}</p>
                </div>

            </div>
        </div>
    </section>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
    mounted: function () {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
            const horSection = gsap.utils.toArray(".port__item");

            gsap.to(horSection, {
                xPercent: -120 * (horSection.length - 1),
                ease: "none",
                scrollTrigger: {
                    trigger: "#port",
                    start: "top 56px",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    markers: false,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                }
            });
        }
    }
}


</script>

<style lang="scss">
#port {
    width: 100%;
    overflow: hidden;
}

.port__inner {
    padding: 16px;
}

.port__title {
    position: sticky;
    top: 70px;
    left: 0;
    width: 70%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    font-family: var(--mainKor-font);
    text-transform: uppercase;
    color: var(--white200);
    border-bottom: 0.4vw solid var(--white200);
    margin-bottom: 100px;
}

.port__title em {
    font-size: 1.25rem;
    font-weight: 400;
    line-height: 2;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
}

.port__item {
    width: 500px;
    height: 70vh;
    background-color: var(--white200);
    margin-right: 20px;
}

.port__item a img {
    padding-left: 30px;
    padding-right: 30px;
    padding-bottom: 16px;
}

.port__item .num {
    font-weight: 800;
    font-size: 2rem;
    padding-left: 26px;
    font-family: var(--mainKor-font);
}

.port__item .title {
    font-weight: 800;
    font-size: 1.8rem;
    text-align: center;
    padding-bottom: 10px;
    border-bottom: 4px solid #cdb9ee;
    font-family: var(--mainKor-font);
}

.port__item .desc {
    padding: 16px;
    font-size: 1.2rem;
    font-family: var(--mainKor-font);
}
</style>