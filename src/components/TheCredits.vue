<template>
    <div class="section section-vfx">
        <div class="container d-flex flex-column justify-content-center px-5">
            <h3>Design & Development:</h3>
            <h3 class="pb-5">@fonzhousefonzie</h3>

            <h3>Original illustrations:</h3>
            <h3><a href="https://it.freepik.com/autore/upklyak">@upklyak</a></h3>
            <h3><a href="https://it.freepik.com/autore/vectorpouch">@vectorpouch</a></h3>

            <h4 class="pt-4 opacity-50">Made with <span class="iconify" data-icon="logos:vue"></span>ue CLI</h4>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
.section-vfx {
    z-index: 2;

    .container {
        transition: 300ms ease-in;

        a {
            font-weight: 600;
            transition: 300ms ease-out;

            &:hover {
                color: var(--blue);
                transform: scale(120%);
                font-weight: 700;
            }

            &:active {
                color: var(--pink);
            }
        }
    }
}
</style>