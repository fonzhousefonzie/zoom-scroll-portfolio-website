<template>
    <div class="section">
        <div class="container d-flex align-items-center px-5">
            <div class="col-50 text-container">
                <h1>Hello, I'm Arturo Arnò</h1>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Repellendus harum ratione labore nam, nobis fuga minus ad, neque dolorum dolor veniam omnis ex accusantium nostrum, provident voluptatum illo tempore quidem!</p>
                <button class="primary-btn" @click="goToContacts()">Something</button>
            </div>
            <div class="col-50 image-container">
                <div class="image">
                    <img src="../assets/img/ArturoArnò.jpg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    methods:{
        goToContacts(){
            window.scrollTo(0, 1600);
        }
    }

}
</script>

<style scoped lang="scss">
.section{
    position: relative;
    z-index: 4;
    .container{
        .text-container{
            text-align: left;
            h1, p{
                padding-bottom: 1rem;
            }
        }
        .image-container{
            .image{
                margin: auto;
                max-width: 300px;
                border-radius: 1rem;
                overflow: hidden;
                box-shadow: 1rem 1rem 0 var(--blue);
            }
        }
    }
}
</style>