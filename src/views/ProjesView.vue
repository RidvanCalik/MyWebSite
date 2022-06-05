<template>
    <div class="row">
        <a class="githubUrl" target="_blank" href="https://github.com/RidvanCalik">Github Hesabım</a>
        <div class="project" v-for="repo in repos" :key="repo.id">
            <a class="projectUrl" target="_blank" :href="repo.html_url">
                <div class="projectContent1">
                    <img :src="repo.owner.avatar_url">
                    <h4>{{ repo.owner.login }}</h4>

                </div>

                <div class="projectContent2">
                    <h2>{{ repo.name }} </h2>
                    <h3>Kullanılan Dil ve diller: {{ repo.language }}</h3>
                    <p>{{ repo.description }}</p>
                    <h5>Son güncelleme: {{ new Date(repo.updated_at).toLocaleDateString() }}</h5>
                </div>
            </a>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
var repos = ref([]);
onMounted(() => {
    fetch("https://api.github.com/users/RidvanCalik/repos").then(response => response.json())
        .then((data) => {
            data.forEach(repo => {

                if (repo.language != null) {
                    repos.value.push(repo);
                }
            });
        });

})
</script>

<style>
.row {
    max-width: 1400px;
    width: 100%;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    padding: 20px 20px;
    gap: 20px;
}

.row .githubUrl {
    font-size: 2em;
    text-decoration: none;
    color: green;
    border-left: 2px solid green;
    transition: border 200ms;
}

.row .githubUrl:hover {

    border-left: 9px solid green;
}


.row .project .projectUrl {
    text-decoration: none;
    color: var(--color-text);
    display: grid;
    grid-template-columns: 15% 85%;
    gap: 20px;
    align-items: center;

    border: 4px solid green;
    width: 100%;
    height: 250px;
    transition: background-color 200ms;
}

.row .project .projectUrl:hover {
    background-color: green;

}

.row .project .projectUrl:hover>* {
    color: white;

}

.row .project .projectUrl .projectContent1 {
    display: grid;
    text-align: center;
    justify-content: center;
    grid-template-rows: 75% 25%;
    height: 100%;
    width: 100%;
    overflow: hidden;
    align-items: center;
}

.row .project .projectUrl .projectContent1 img {
    width: 140px;
    height: 140px;
    object-fit: cover;
    border-radius: 50%;


}

.row .project .projectUrl .projectContent1 h2 {
    flex: 2;
}


.row .project .projectUrl .projectContent2 {
    height: 100%;
    width: 97%;
    display: flex;
    flex-direction: column;

}

.row .project .projectUrl .projectContent2 p {
    width: 90%;
    margin-top: 2px;
    flex-grow: 1;

}

.row .project .projectUrl .projectContent2 h5 {
    align-self: flex-end;
}



@media (max-width: 846px) {
    .row .project .projectUrl {
        height: 200px;
        grid-template-columns: 30% 70%;
        gap: 2px;
    }

    .row .project .projectUrl .projectContent1 {
        grid-template-rows: 50% 50%;

    }

    .row .project .projectUrl .projectContent2 {
        font-size: .8em;

    }

    .row .project .projectUrl .projectContent1 img {
        width: 80px;
        height: 80px;
    }

}
</style>