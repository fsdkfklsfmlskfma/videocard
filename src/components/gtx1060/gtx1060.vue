<template>
  <div class="root">
    <div class="main-card" @click="show1060Modal = true">
      <img class="card-image1060" src="./1060.png" />
       <div class="image-overlay image-overlay__primary">
        <p class="image-title">Информация</p>        
      </div>

      <h1 class="card-header">GTX 1060</h1>

      <p class="card-text">
  GeForce GTX 1060 6 ГБ — видеокарта высокопроизводительного сегмента от NVIDIA, выпущенная 19 июля 2016 года.
      </p>
    </div>

    <Teleport to="body">
      <Modal 
        :show="show1060Modal"
        @close="show1060Modal = false"
      />
    </Teleport>
  </div>
</template>

<script>
import Modal from './modal1060.vue'

  export default {
    components: {
      Modal,
    },

    data: () => ({
      show1060Modal: false,
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
.card-image1060 {
  transform: rotate(20deg);
  height: 160px;
  width: 200px;
}
</style>