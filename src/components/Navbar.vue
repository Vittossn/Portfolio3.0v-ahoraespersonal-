<script setup>
import { ref, onMounted } from 'vue';
const ul = ref(null)
const props = defineProps(['showNav', 'isComputer'])
const tagsHeader = ['Home','Projects','Skills','About']
const ulshow = () => {
    const list = ul.value.querySelectorAll('li')
}
onMounted(()=>{
    window.addEventListener('click', ulshow)
})
</script>
<template>
    <header v-if="props.isComputer">
        <Transition name="visibility">
            <ul v-if="showNav"  key="component" class="comp-animated" ref="ul">
                <li v-for="tag in tagsHeader" :key="tag">
                <a :href="'#'+tag" ref="tagsHeader">{{ tag }}</a>
                </li>
            </ul>
        </Transition>
    </header>
</template>
<style scoped>
header {
    z-index: 100;
    height: 36vh;
    position: fixed;
    top: 32vh;
    display: flex;
    flex-direction: column;
    left: .5vw;
}
ul{
    padding: 0;
}

ul li a {
    color: #6d2def;
    text-decoration: none;
    transition: all ease .5s;
    font-size: 1.5rem;
    font-weight: bold;
}

ul li a:hover {
    color: #6532cc;
    border-bottom: solid 5px #9370db;
}

ul li {
    transition: transform .5s ease;
    list-style: none;
    margin: 2vh 0;
    text-align: start;
}
ul li:hover{
    transform: translateX(15px);
}
.visibility-enter-active {
    transition: all 1s ease;
}
.visibility-leave-active {
    transition: all .5s ease;
}
.visibility-enter-from, .visibility-leave-to{
    opacity: 0;
    transform: translateX(-40px);
}
</style>