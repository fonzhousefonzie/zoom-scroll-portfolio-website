<template>
    <div class="section section-vfx" id="contacts">
        <div class="container d-flex align-items-center">
            <div class="col-50 image-container">
                <div class="image">
                    <img src="../assets/img/contacts.svg" alt="">
                </div>
            </div>
            <div class="col-50 text-container">
                <h2 class="pb-4">Let's get in touch!</h2>
                <form action="" method="post">
                    <div class="d-flex gap-3 pb-3">
                        <input class="form-control" type="text" name="name" id="name" placeholder="What's your name?">
                        <input class="form-control" type="email" name="email" id="email" placeholder="What's your email?">
                    </div>
                    <textarea class="form-control mb-3 p-3" name="text" id="text" cols="30" rows="7" placeholder="Ask me any question, I'll be happy to answer you as soon as possible!"></textarea>
                    <input type="submit" class="button primary-btn large-btn" value="Send">
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
.section-vfx {
    z-index: 1;
    .container{
        .image{
            img{
                max-width: 100%;
            }
        }

        .text-container{
            padding-right: 3rem;
            form{
                textarea{
                    height: inherit;
                }
            }
        }
    }
}

@media screen and (max-width: 992px) {
    .section {

        .container {

            .col-50 {
                width: 100%;
            }

            .image-container {
                display: none;
            }

            .text-container{
                padding-right: 0;
            }
        }
    }
}
</style>