<script setup>
function dowloadCV() {
  window.open("/ridvancalikCV.pdf");
}
</script>
<template>
  <div class="row">
    <div class="left-side">
      <img src="@/assets/profile2.jpg">
      <a @click="dowloadCV()">CV indir</a>

    </div>
    <div class="right-side">
      <h1>Frontend geliştirici</h1>
      <br>
      <h3>&emsp;&emsp;Şehit Büyük Elçi İsmail Erez MTAL' de Bilişim teknolojileri & Web programala alanından mezun
        olduktan
        sonra
        alaylı olarak yazılım kariyerime devam etmekteyim</h3>
      <br>
      <h2>Sertifikalarım</h2>
      <div>&emsp;&emsp;<a target="_blank"
          href="https://gelecegiyazanlar.turkcell.com.tr/kisi/belge/ridvancalik/Web%20Programlama/101">Web
          Programlama 101</a></div>
      <br>

      <h2>
        Bildiğim ve Öğreniyor olduğum teknolojiler</h2>
      <nav>
        <li>HTML</li>
        <li>CSS</li>
        <li>JS</li>
        <li>VUE.JS</li>
        <li>REACT.JS</li>
        <li>BOOTSTRAP</li>
        <li>MYSQL</li>
        <li>PHP</li>
        <li>FLUTTER</li>
      </nav>
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
  padding: 0 150px;
  height: 100%;
  display: flex;

  justify-content: center;

  flex-direction: column;
  text-align: left;
}

.right-side nav {

  flex-wrap: wrap;
  overflow: hidden;
  display: flex;
}

.right-side li {
  cursor: default;
  text-align: center;
  min-width: 90px;
  list-style: none;
  border-radius: 500px;
  padding: .3em;
  margin: .4em;

  transition: all 200ms;
  color: var(--byridvan);
  border: 2px solid green;
}

.right-side li:hover {
  color: whitesmoke;
}

.right-side a {
  text-decoration: none;

  margin: 0.3em;
  color: green;
  border-left: 2px solid green;
  transition: border 400ms;
}

.right-side a:hover {

  border-left: 15px solid green;
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

.left-side a {
  box-shadow: none;
  border: none;
  max-width: 60%;
  text-align: center;
  margin: 60px;

  font-size: 15px;
  border-left: 2px solid green;

  display: inline-block;
  background-color: none;
  text-decoration: none;
  background-color: var(--color-background);
  cursor: pointer;
  color: green;
  transition: all 400ms;
}

.left-side a:hover {
  border-left: 15px solid green;

}

@media (max-width: 1024px) {
  .row {

    grid-template-columns: 50% 50%;
  }

  .right-side {
    padding: 0 10px;

  }
}

@media (max-width: 846px) {
  .row {
    min-height: 150%;
    grid-template-columns: 90%;
    grid-template-rows: 50% 90%;


  }

  .right-side {
    padding: 0 10px;

  }
}
</style>
