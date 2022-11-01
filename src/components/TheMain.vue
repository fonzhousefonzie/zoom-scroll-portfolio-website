<template>
    <main :class="{ 'main-scrolled-once': scrollPx >= 300}">
        <div class="overlay">
            <AboutMe :class="{ 'whenScrolled': scrollPx >= 300}" />
            <LastWorks :class="{ 'beforeScroll': scrollPx < 300, 'whenScrolled': scrollPx >= 700}" />
            <MySkills :class="{ 'beforeScroll': scrollPx < 700 , 'whenScrolled': scrollPx >= 1100}" />
            <WebDev :class="{ 'beforeScroll': scrollPx < 1100, 'whenScrolled': scrollPx >= 1500}" />
            <ContactsSection :class="{ 'beforeScroll': scrollPx < 1500 , 'whenScrolled': scrollPx >= 1900}" />
            <TheCredits :class="{ 'beforeScroll': scrollPx < 1900 }" />
        </div>
    </main>
</template>

<script>
import WebDev from './WebDev.vue';
import AboutMe from './AboutMe.vue';
import MySkills from './MySkills.vue';
import ContactsSection from './ContactsSection.vue';
import TheCredits from './TheCredits.vue';
import LastWorks from './LastWorks.vue';
export default {
    components: { WebDev, AboutMe, MySkills, ContactsSection, TheCredits, LastWorks },
    data() {
        return {
            scrolled: false,
            scrollPx: 0,
            zoomEffect: true,
        };
    },
    methods: {
        handleScroll() {
            this.scrolled = window.scrollY > 0;
            this.scrollPx = window.scrollY;
        }
    },
    created() {
        window.addEventListener('scroll', this.handleScroll);
    },
    destroyed() {
        window.removeEventListener('scroll', this.handleScroll);
    }
}
</script>

<style scoped lang="scss">
main {
    min-height: 3000px;
    background: url(../assets/img/farid-askerov-cX6ra6dCtAM-unsplash.jpg);
    background-size: 100% 100vh;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    overflow: auto;
    position: relative;
    z-index: 0;
    transition: background 300ms ease;

    .overlay {
        background: rgba(0, 0, 0, 0.5);
        position: fixed;
        top: 0;
        right: 0;
        left: 0;
        bottom: 0;
        z-index: -1;

        div {
            transition: 300ms ease;
        }

        .section-vfx {
            max-height: 100%;
            overflow: hidden;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
        }

        .whenScrolled {
            transform: scale(300%);
            opacity: 0;
            pointer-events: none;
        }

        .beforeScroll {
            transform: scale(0.1);
            opacity: 0;
        }
    }
}

.main-scrolled-once {
    background: url(../assets/img/victor-elvira-avalos-tb8G24Fw_ks-unsplash.jpg);
    background-size: 100% 100vh;
    background-position: center;
    background-repeat: no-repeat;
    background-attachment: fixed;
}
</style>