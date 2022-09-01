<template>
    <div class="section d-flex">
        <div class="container d-flex align-items-center">
            <div class="col-50 text-container pt-4">
                <h2>My Skills</h2>
                <div class="d-flex p-3 justify-content-between flex-wrap align-content-start gap-3">
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
                    rating: 99
                },
                {
                    name: 'CSS',
                    rating: 98
                },
                {
                    name: 'SCSS',
                    rating: 90
                },
                {
                    name: 'JavaScript',
                    rating: 76
                },
                {
                    name: 'Pinco',
                    rating: 100
                },
                {
                    name: 'Palla',
                    rating: 50
                },
                {
                    name: 'MySQL',
                    rating: 60
                },
                {
                    name: 'Vue JS',
                    rating: 65
                },
                {
                    name: 'Gianfranco',
                    rating: 35
                },
                {
                    name: 'Mario',
                    rating: 80
                },
            ]
        }
    }
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

        .image-container {
            .image {
                img {
                    max-width: 100%;
                }
            }
        }

        .text-container {
            .range {
                width: 15rem;
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
    .scale{
        transform: scale(500%);
        opacity: 0;
    }
}
</style>