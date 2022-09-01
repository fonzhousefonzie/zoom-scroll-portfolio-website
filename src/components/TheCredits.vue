<template>
    <div class="section">
        <div class="container d-flex flex-column justify-content-center px-5">
            <h3>Design & Development:</h3>
            <h3 class="pb-5">@fonzhousefonzie</h3>

            <h3>Original illustrations:</h3>
            <h3><a href="https://it.freepik.com/autore/upklyak">@upklyak</a></h3>
            <h3><a href="https://it.freepik.com/autore/vectorpouch">@vectorpouch</a></h3>

            <h4 class="pt-4 opacity-50">Made with <iconify-icon icon="logos:vue"></iconify-icon>ue CLI</h4>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
.section {
    max-height: 100%;
    overflow: hidden;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
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