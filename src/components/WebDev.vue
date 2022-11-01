<template>
    <div class="section section-vfx">
        <div class="container d-flex align-items-center">
            <div class="col-50 image-container">
                <div class="image">
                    <img src="../assets/img/education.svg" alt="">
                </div>
            </div>
            <div class="col-50 text-container">
                <h3>Self-taught</h3>
                <div class="d-flex align-items-center w-100 px-5 pt-3 pb-2 justify-content-evenly">
                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:adobe-photoshop"></span>
                        <p>Photoshop</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:adobe-illustrator"></span>
                        <p>Illustrator</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:figma"></span>
                        <p>Figma</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="majesticons:ux-circle-line"
                            style="color: white;"></span>
                        <p>User Experience</p>
                    </div>
                </div>
                <div class="d-flex align-items-center w-100 px-5 pt-3 pb-5 justify-content-evenly">

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:html-5"></span>
                        <p>HTML5</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:css-3"></span>
                        <p>CSS3</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:sass"></span>
                        <p>SASS</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="vscode-icons:file-type-js-official"></span>
                        <p>JavaScript</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" style="color:red;" data-icon="cib:filezilla"></span>
                        <p>FileZilla</p>
                    </div>
                </div>


                <h3>Boolean Careers</h3>
                <div class="d-flex align-items-center w-100 px-5 pt-3 pb-2 justify-content-between">

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:visual-studio"></span>
                        <p>VS Code</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:git-icon"></span>
                        <p>Git</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:bootstrap"></span>
                        <p>Bootstrap</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:npm-icon"></span>
                        <p>npm</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="vscode-icons:file-type-node"></span>
                        <p>Node.js</p>
                    </div>
                </div>

                <div class="d-flex align-items-center w-100 px-5 pt-3 pb-5 justify-content-between">

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:vue"></span>
                        <p>Vue</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="simple-icons:mamp" style="color: #2479aa;"></span>
                        <p>MAMP</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="vscode-icons:file-type-composer" style="color: #2479aa;"></span>
                        <p>Composer</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:php"></span>
                        <p>PHP</p>
                    </div>

                    <div class="text-center px-3 pt-3 border">
                        <span class="iconify fs-1 pb-1" data-icon="logos:laravel"></span>
                        <p>Laravel</p>
                    </div>
                </div>
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
    z-index: 3;

    .container {
        .image-container {
            .image {
                img {
                    max-width: 100%;
                }
            }
        }

        .text-container {
            .text-center.border {
                backdrop-filter: blur(0.1rem);
                border-color: rgba(0, 0, 0, 0) !important;
                border-radius: 0.5rem;
                box-shadow: inset 0 0 1rem rgba(245, 245, 245, 0.5);
            }
        }
    }
}
</style>