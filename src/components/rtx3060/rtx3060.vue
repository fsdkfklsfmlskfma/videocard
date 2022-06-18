<template>
  <div class="root">
    <div class="main-card" @click="show3060Modal = true">
      <img class="card-image3060" src="./3060.png" />
             <div class="image-overlay image-overlay__primary">
        <p class="image-title">Информация</p>        
      </div>
      <h1 class="card-header">RTX 3060</h1>

      <p class="card-text">
GeForce RTX 3060 — это видеокарта высокопроизводительного сегмента от NVIDIA, выпущенная 12 января 2021 года.
      </p>
    </div>

    <Teleport to="body">
      <Modal 
        :show="show3060Modal"
        @close="show3060Modal = false"
      />
    </Teleport>
  </div>
</template>

<script>
import Modal from './modal3060.vue'

  export default {
    components: {
      Modal,
    },

    data: () => ({
      show3060Modal: false,
    })
  };

</script>

<style>
.main-card {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

  font-family: "Geforce";
  color: #00ff29;

  background-color: black;
  box-shadow: 10px 10px 10px rgba(24, 24, 24, 0.379);

  margin-top: 30px;
  margin-right: 62px;

  padding: 10px;

  width: 220px;
  height: 350px;
}

.card-text {
  color: #fff;
  font-weight: bold;
  font-size: 18px;
}
.card-image3060 {
  transform: rotate(23deg);
  height: 160px;
  width: 200px;
}
</style>