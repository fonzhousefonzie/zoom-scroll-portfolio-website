<template>
    <div class="section" id="contacts">
        <div class="container d-flex align-items-center">
            <div class="col-50 image-container">
                <div class="image">
                    <img src="../assets/img/contacts.svg" alt="">
                </div>
            </div>
            <div class="col-50 text-container pe-5">
                <h2 class="pb-5">Conosciamoci!</h2>
                <form action="" method="post">
                    <div class="d-flex gap-3 pb-3">
                        <input class="form-control" type="text" name="name" id="name" placeholder="Come ti chiami?">
                        <input class="form-control" type="email" name="email" id="email" placeholder="Qual è la tua email?">
                    </div>
                    <textarea class="form-control mb-3 p-3" name="text" id="text" cols="30" rows="10" placeholder="Fammi qualsiasi domanda, sarò felice di risponderti al più presto!"></textarea>
                    <input type="submit" class="button primary-btn large-btn" value="Invia">
                </form>
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
    z-index: 1;
    .container{
        .image{
            img{
                max-width: 100%;
            }
        }
    }
}
</style>