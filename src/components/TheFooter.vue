<template>
    <footer>
        <div class="container d-flex justify-content-between align-items-center">
            <div class="icons d-flex">
                <a href="#">
                    <i class="fa fa-brands fa-instagram px-3"></i>
                    <div class="hover-bg"></div>
                </a>
                <a href="#">
                    <i class="fa fa-brands fa-linkedin px-3"></i>
                    <div class="hover-bg"></div>
                </a>
                <a href="#">
                    <i class="fa fa-brands fa-whatsapp px-3"></i>
                    <div class="hover-bg"></div>
                </a>
                <a href="#">
                    <i class="fa fa-brands fa-github px-3"></i>
                    <div class="hover-bg"></div>
                </a>
            </div>
            <div class="copy text-end d-flex align-items-center">
                <div class="text">
                    <p>Love is the answer</p>
                    <p>&copy; <span>Fonzhousefonzie</span> 2022</p>
                </div>
                <i class="fa fa-solid fa-heart"></i>
            </div>
        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">
footer {
    background: linear-gradient(transparent, var(--black));
    padding: 3rem 0rem 2rem;
    color: whitesmoke;
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
    z-index: 10;

    .icons {
        font-size: 1.5rem;

        a {
            position: relative;
            z-index: 10;

            i {
                position: relative;
                z-index: 10;
            }

            .hover-bg {
                pointer-events: none;
                position: absolute;
                top: 10rem;
                left: 0;
                right: 0;
                background: linear-gradient(135deg, var(--pink), var(--blue));
                height: 7rem;
                z-index: 9;
                padding: 0.5rem 0;
                border-radius: 0.5rem 0.5rem 0 0;
                transition: 200ms ease-out;
            }

            &:hover .hover-bg {
                top: -0.5rem;
            }
        }
    }

    .copy {
        cursor: default;
        &:hover i{
            animation: beat 500ms linear;
        }

        .text{
            padding-right: 0.5rem;
            border-right: 1px solid var(--pastel-pink);

        p {
            margin: 0;
            color: var(--pastel-pink);
            font-size: 0.8rem;

            span {
                background: linear-gradient(135deg, var(--pink), var(--blue));
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
            }
        }
        }

        i {
            font-size: 1.5rem;
            padding-left: 0.5rem;
            background: linear-gradient(135deg, var(--pink), var(--blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    }
}

@keyframes beat {
    from, to{
        transform: scale(100%);
    }
    35%{
        transform: scale(120%);
    }
    50%{
        transform: scale(100%);
    }
    65%{
        transform: scale(120%);
    }
}
</style>