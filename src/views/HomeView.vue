<script setup>
function dowloadCV() {
  window.open("../public/ridvancalikCV.pdf");
}
</script>
<template>
  <div class="row">
    <div class="left-side">
      <img src="@/assets/profile2.jpg">
      <button @click="dowloadCV">CV indir</button>

    </div>
    <div class="right-side">
      <h1>Frontend geliştirici</h1>
      <h2>Frontend geliştirici</h2>
      <hr>
      <h2>Bildiğim ve Öğreniyor olduğum teknolojiler</h2>
      <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JS</li>

      </ul>
      <ul>
        <li>MYSQL</li>
        <li>PHP</li>
        <li>FLUTTER</li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.row {
  display: grid;
  grid-template-columns: 30% 70%;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100%;

}



.left-side {
  display: grid;
  align-items: center;
  justify-items: center;
  grid-template-columns: 100%;
  grid-template-rows: 50% 50%;
}

.right-side {

  height: 100%;
  display: grid;

  justify-content: center;
  align-items: center;

  grid-template-columns: 50% 50%;
  grid-template-rows: 50% 5% 1% 15% 29%;
  text-align: center;
}

.right-side>* {
  grid-column-start: 1;
  grid-column-end: 3;

}

.right-side :nth-last-child(1) {
  grid-column-start: 2;
  grid-column-end: 3;

}

.right-side :nth-last-child(2) {
  grid-column-start: 1;
  grid-column-end: 2;
}

ul {
  list-style: none;
  display: inline-block;
  text-align: center;
}


.left-side img {
  width: 300px;
  height: 300px;
  border: 4px solid green;
  border-radius: 300px;
  object-fit: cover;

}

button {
  box-shadow: none;
  border: none;
  max-width: 50%;
  text-align: center;
  margin: 20px;
  padding: 25px;
  display: inline-block;
  line-height: 10px;
  border-radius: 50px;
  transition: background-color 700ms;
  background-color: green;
  text-decoration: none;
  color: white;
}

@media (max-width: 1024px) {
  .row {

    grid-template-columns: 50% 50%;
  }
}

@media (max-width: 846px) {
  .row {
    min-height: 200%;
    grid-template-columns: 90%;
    grid-template-rows: 70% 50%;


  }
}
</style>
