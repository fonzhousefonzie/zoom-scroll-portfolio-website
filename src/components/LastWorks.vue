<template>
    <div class="section section-vfx">
        <div class="container">
            <h2>My last works</h2>

            <div id="carouselExampleDark" class="carousel slide" data-bs-ride="carousel">
                <div class="carousel-indicators">
                    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active"
                        aria-current="true" aria-label="Slide 1"></button>
                    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1"
                        aria-label="Slide 2"></button>
                    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="2"
                        aria-label="Slide 3"></button>
                </div>
                <div class="carousel-inner">
                    <div class="carousel-item carousel-size" data-bs-interval="10000">
                        <img src="../assets/img/1.png" class="d-block w-75 m-auto" alt="image">
                        <div class="carousel-caption p-3 d-md-block">
                            <h5>Deliveboo App</h5>
                            <p>A web application for food delivery, with backoffice and email service.</p>
                        </div>
                    </div>
                    <div class="carousel-item active carousel-size" data-bs-interval="2000">
                        <img src="../assets/img/2.png" class="d-block w-75 m-auto" alt="image">
                        <div class="carousel-caption p-3 d-none d-md-block">
                            <h5>DC Comics Clone</h5>
                            <p>A responsive clone of DC Comics website, with comic details, made with VueCLI</p>
                        </div>
                    </div>
                    <div class="carousel-item carousel-size">
                        <img src="../assets/img/3.jpg" class="d-block w-75 m-auto" alt="image">
                        <div class="carousel-caption p-3 d-none d-md-block">
                            <h5>Prisma: collective art exhibition</h5>
                            <p>A static website for an art exhibition where I exhibited some of my artworks.</p>
                        </div>
                    </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleDark"
                    data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleDark"
                    data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                </button>
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
    z-index: 2;

    .container {
        transition: 300ms ease-in;

        .carousel-size {
            height: 70vh;
            overflow: hidden;

            .carousel-caption {
                background-color: rgba(var(--dark-rgb), 0.7);
                backdrop-filter: blur(0.1rem);
                border-color: rgba(0, 0, 0, 0);
                border-radius: 0.5rem;
                box-shadow: inset 0 0 1rem rgba(245, 245, 245, 0.5);
            }
        }
    }
}
</style>