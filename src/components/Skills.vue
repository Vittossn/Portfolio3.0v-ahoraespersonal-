<script setup>
 const props = defineProps(['isComputer'])
</script>
<template>
    <aside class="div" >
    <section id="Skills" :class="isComputer ? '':'sectionres'">
        <h1 :class="isComputer ? '' : 'h1res'">Skills</h1>
        <div >
            <article :class="isComputer ? '' : 'articleres'">
                <p>Frontend</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/htmlImg.svg" alt="HTML5" title="HTML5">
                    <img src="../../src/assets/img/cssImg.svg" alt="CSS3" title="CSS3">
                    <img src="../../src/assets/img/jsImg.svg" alt="JS" title="JS">
                    <img src="../../src/assets/img/vueImg.svg" alt="Vue.js" title="Vue">
                    <img src="../../src/assets/img/nuxtImg.svg" alt="Nuxt" title="Nuxt">
                    <img src="../../src/assets/img/reactImg.svg" alt="React" title="React">
                </div>
            </article>
            <article :class="isComputer ? '' : 'articleres'">
                <p>Backend</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/nodeImg.svg" alt="Node" title="Node">
                    <img src="../../src/assets/img/expressImg.svg" alt="Express" title="Express">
                    <img src="../../src/assets/img/mongoImg.svg" alt="MongoDB" title="MongoDB">
                    <img src="../../src/assets/img/mongooseImg.svg" alt="Mongoose" title="Mongoose">
                </div>
            </article>
            <article :class="isComputer ? '' : 'articleres'">
                <p>Complementary</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/figmaImg.svg" alt="Figma" title="Figma">
                    <img src="../../src/assets/img/gitImg.svg" alt="Git" title="Git">
                    <img src="../../src/assets/img/githubImg.svg" alt="Github" title="Github">
                    <img src="../../src/assets/img/viteImg.svg" alt="Vite" title="Vite">
                </div>
            </article>
            <article :class="isComputer ? '' : 'articleres'">
                <p>Mobile</p>
                <div class="tecnologias">
                    <img src="../../src/assets/img/dartImg.svg" alt="Dart" title="Dart">
                    <img src="../../src/assets/img/flutterImg.svg" alt="Flutter" title="Flutter">
                </div>
            </article>
        </div>
    </section>
</aside>
</template>
<style scoped>
.div{
    width: 100%;
    height: max-content;
}
section{
    margin: 0 auto;
    height: max-content;
    width: 80%;
    background:transparent;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: flex-start;
}
h1{
    font-size: 3rem;
    color: #C0C0C0;
}
.h1res{
    margin-left: 2.8rem;
}
.container{
    display: flex;
    width: 100%;
    justify-content: center;
    flex-wrap: wrap;
}
.sectionres{
    margin: 0;
    width: 100%;
}
article{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: #202020;
    width: 30%;
    height: 50vh;
    margin: .5rem 1rem;
    border-radius: .8rem;
    border-bottom: 3px solid #9370db;
    border-right: 3px solid #9370db;
}
.articleres{
    width: 80%;
}
p{
    margin: .5rem 0;
    text-align: center;
    width: 100%;
    font-size: 1.5rem;
}
div{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}
.tecnologias{
    height: 35vh ;
}
img{
    margin:.3rem;
}
</style>