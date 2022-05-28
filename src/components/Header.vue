<template>
    <div class="Header">
        <h2 class="title">PORTFOLYO / Rıdvan Çalık</h2>
        <ul class="nav-md">
            <li>
                <router-link to="/">Anasayfa</router-link>
            </li>
            <li>
                <router-link to="/projes">Projelerim</router-link>
            </li>
            <li>
                <router-link to="/contact">İletişim</router-link>
            </li>
        </ul>
        <i @click="toogleModal()" style="font-size:48px; cursor:pointer;" class="material-icons hamburger">menu</i>


    </div>
    <div @click="toogleModal()" id="modal" :class="{ showModal: modal, hiddenModal: !modal }">

        <h1>
            <router-link to="/">Anasayfa</router-link>
        </h1>
        <h1>
            <router-link to="/projes">Projelerim</router-link>
        </h1>
        <h1>
            <router-link to="/contact">İletişim</router-link>
        </h1>



    </div>


</template>

<script setup>

import { ref } from 'vue';
var modal = ref(false);

function toogleModal() {
    modal.value = !modal.value;
}
</script>

<style scoped>
a {
    color: white;
    text-decoration: none;
}

.Header {
    padding: 5px;
    max-width: 100%;
    margin: 20px auto;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.title {
    display: inline-block;
}

.title:hover {
    color: green;
}

.hamburger {
    display: none;
}

.showModal {
    transform: translateX(0%);
}

.hiddenModal {
    transform: translateX(100%);
}

#modal {

    left: 0%;
    top: 0;
    position: fixed;
    z-index: 1000;
    background-color: gray;
    min-width: 100%;
    min-height: 100%;
    transition: 500ms;
    opacity: 0.8;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    gap: 60px;
    justify-content: center;
    align-items: center;
}


.nav-md {
    display: inline-block;
    list-style: none;

}

.nav-md li {
    margin: 20px;
    padding: 25px;
    display: inline-block;
    line-height: 10px;
    border-radius: 50px;
    transition: background-color 700ms;
}

.nav-md li:hover {
    cursor: pointer;
    color: white;
    background-color: green;
}

@media (max-width: 846px) {
    .nav-md {
        display: none;

    }

    .hamburger {
        display: block;
    }
}
</style>