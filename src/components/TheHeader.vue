<template>
    <header>
        <div class="container header d-flex justify-content-between align-items-center">
            <div class="logo d-flex">
                <img src="../assets/img/fonzieColor.png" alt="Fonzhousefonzie Logo">
                <p class="logo-title">Fonzhousefonzie</p>
            </div>
            <p class="menu" @click="dropdownShow()" :class="{ 'active': dropdown }" tabindex="0" @focusout="clickOut()">
                <i class="fa-solid fa-bars"></i><span> Menu</span>
            </p>
        </div>
        <div class="container dropdown">
            <ul class="dropdown-content" :class="{ 'dropdown-show': dropdown }">
                <li><a href="#about">About</a></li>
                <li><a href="#works">Last works</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#edu">Front-End</a></li>
                <li><a href="#contacts">Contacts</a></li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            dropdown: false
        }
    },
    methods: {
        dropdownShow() {
            this.dropdown = !this.dropdown;
        },
        clickOut() {
            this.dropdown = false;
        }
    },
    mounted() {
        this.clickOut()
    }
}
</script>

<style lang="scss" scoped>
header {
    padding: 0rem 0rem 3rem;
    color: whitesmoke;
    font-weight: 600;
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    z-index: 9;

    .container.header {
        background: linear-gradient(135deg, rgba(var(--dark-rgb), 0.8) 10%, rgba(var(--pink-rgb), 0.7) 40%, rgba(var(--blue-rgb), 0.7) 60%, rgba(var(--dark-rgb), 0.8) 90%);
        box-shadow: inset 0 0 2rem rgba(255, 255, 255, 0.1);
        border-radius: 0 0 1rem 1rem;
        position: relative;
        z-index: 10;
        padding: 1rem 1rem;
        pointer-events: none;

        .logo {
            align-items: center;

            img {
                max-height: 70px;
            }

            .logo-title {
                padding: 1rem;
                margin: 0;
                font-weight: 600;
                font-size: 1.5rem;
            }
        }

        .menu {
            cursor: pointer;
            padding: 0.7rem 2rem;
            margin: 0;
            border-radius: 0.5rem;
            background: linear-gradient(135deg, var(--blue), var(--pink), var(--blue));
            background-size: 200%;
            background-position: left;
            transition: 200ms linear;
            pointer-events: all;

            &:hover {
                background-position: right;
            }
        }

        .active {
            color: var(--cyan);
        }
    }

    .container.dropdown {
        pointer-events: none;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 10;

        .dropdown-content {
            pointer-events: none;
            position: absolute;
            filter: blur(10rem);
            opacity: 0;
            top: -15rem;
            right: 1rem;
            transition: 300ms ease-out;

            li {
                padding: 0;

                a {
                    margin: 0.5rem 0;
                    padding: 0.5rem 1.4rem;
                    width: 100%;
                    background: linear-gradient(135deg, var(--blue) 0%, var(--pink) 20%, rgba(var(--dark-rgb), 0.7) 80%, rgba(var(--blue-rgb), 0.5) 105%);
                    background-size: 300%;
                    background-position: right;
                    border-radius: 0.5rem;
                    transition: 300ms ease-in;

                    &:hover {
                        background-position: left;
                    }
                }
            }
        }

        .dropdown-show {
            top: 7rem;
            opacity: 1;
            filter: blur(0rem);
            pointer-events: all;
        }
    }
}

@media screen and (max-width: 767px) {
    header {
        .container.header {
            padding: 0.5rem 1rem;

            .logo {
                padding-left: 0.5rem;

                img {
                    max-height: 50px;
                    aspect-ratio: 43/50;
                }

                .logo-title {
                    font-size: 1.2rem;
                }
            }

            .menu {
                padding: 0.7rem 1.1rem;

                span {
                    display: none;
                }
            }
        }

        .container.dropdown {
            .dropdown-content {
                right: 0;
                left: 0;
                padding: 0 2rem;

                li {
                    a {
                        font-size: 1.2rem;
                        background: linear-gradient(135deg, var(--dark) 10%, rgba(var(--pink-rgb), 0.8) 40%, var(--blue) 60%, var(--dark) 90%);
                    }
                }
            }
        }
    }
}

@media screen and (max-width: 327px) {
    header {
        .container.header {

            .logo {

                img {
                    max-height: 40px;
                }

                .logo-title {
                    font-size: 1rem;
                }
            }

            .menu {
                padding: 0.5rem 0.8rem;
                font-size: 0.8rem;
            }
        }
    }
}
</style>