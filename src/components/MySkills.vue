<template>
    <div class="section section-vfx">
        <div class="container d-flex align-items-center">
            <div class="col-50 text-container pt-4">
                <h2>My Skills</h2>
                <div class="d-flex p-3 justify-content-center flex-wrap align-content-start gap-4">
                    <div v-for="skill in skills" :key="skill.name">
                        <p>{{ skill.name }}</p>
                        <div class="range">
                            <div class="range-bar" :style="'width: ' + skill.rating + '%'"></div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-50 image-container">
                <div class="image">
                    <img src="../assets/img/WEBdEVdES.svg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            skills: [
                {
                    name: 'HTML',
                    rating: 95
                },
                {
                    name: 'CSS',
                    rating: 100
                },
                {
                    name: 'SCSS',
                    rating: 70
                },
                {
                    name: 'JavaScript',
                    rating: 92
                },
                {
                    name: 'Bootstrap',
                    rating: 76
                },
                {
                    name: 'Vue.js',
                    rating: 60
                },
                {
                    name: 'PHP',
                    rating: 72
                },
                {
                    name: 'Figma',
                    rating: 60
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
.section-vfx {
    z-index: 2;

    .container {
        transition: 300ms ease-in;

        .image-container {
            .image {
                img {
                    max-width: 100%;
                }
            }
        }

        .text-container {
            .range {
                width: 13rem;
                height: 0.5rem;
                background: var(--pastel-pink);
                border-radius: 1rem;
                overflow: hidden;

                .range-bar {
                    height: 100%;
                    background-color: var(--blue);
                    border-radius: 1rem;
                }
            }
        }
    }

    .scale {
        transform: scale(500%);
        opacity: 0;
    }
}

@media screen and (max-width: 1200px) {
    .section {

        .container {

            .text-container {

                .range {
                    width: 12rem;
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

            .text-container {

                .range {
                    width: 18rem;
                }
            }
        }
    }
}
</style>