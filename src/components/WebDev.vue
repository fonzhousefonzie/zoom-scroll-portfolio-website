<template>
    <div class="section">
        <div class="container d-flex align-items-center">
            <div class="col-50 image-container">
                <div class="image">
                    <img src="../assets/img/education.svg" alt="">
                </div>
            </div>
            <div class="col-50 text-container">
                
            </div>
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
    z-index: 3;
    .container{
        .image{
            img{
                max-width: 100%;
            }
        }
    }
}
</style>