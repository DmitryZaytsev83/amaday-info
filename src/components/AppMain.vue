<template>
  <div class="container">
    <h2 class="new-release">26 декабря 2020 года официальный релиз нашего альбома "<span class="accent">2020</span>" на
      всех мировых музыкальных
      площадках.</h2>
    <div class="cards">
      <div class="card">
        <div class="text-wrapper">
          <h3>Участники:</h3>
          <h4>Макс Егоров</h4>
          <p>Музыкальный продюсер проекта, автор текстов, музыки, идеи.</p>
          <h4>Леонид Цветков</h4>
          <p>Аранжировщик, звукорежиссёр, сведение, мастеринг, бэк вокал</p>
          <h4>Катерина Герда</h4>
          <p>Вокал, бэк вокал</p>
        </div>
      </div>
      <div class="card">
        <figure class="wrapper2020">
          <img class="img-fluid" src="../assets/album2020.jpg" alt="wrapper">
        </figure>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppMain"
}
</script>

<style scoped>
.new-release {
  margin: 1rem 0;
}

.cards {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.card {
  min-width: 350px;
  max-width: 550px;
  color: yellow;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1rem;
}

.text-wrapper {
  text-align: left;
}

.wrapper2020 {
  width: 100%;
}

.img-fluid {
  width: 100%;
  height: auto;
  border: 1px solid yellow;
}

h3, p {
  color: white;
}

.accent {
  color: yellow;
}
</style>
