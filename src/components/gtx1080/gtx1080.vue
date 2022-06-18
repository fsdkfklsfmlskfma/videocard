<template>
  <div class="root">
    <div class="main-card" @click="show1080Modal = true">
      <img class="card-image1080" src="./1080.png" />

             <div class="image-overlay image-overlay__primary">
        <p class="image-title">Информация</p>        
      </div>
      <h1 class="card-header">GTX 1080</h1>

      <p class="card-text">
   GeForce GTX 1080 — высокопроизводительная видеокарта от NVIDIA, выпущенная 27 мая 2016 года.
      </p>
    </div>

    <Teleport to="body">
      <Modal 
        :show="show1080Modal"
        @close="show1080Modal = false"
      />
    </Teleport>
  </div>
</template>

<script>
import Modal from './modal1080.vue'

  export default {
    components: {
      Modal,
    },

    data: () => ({
      show1080Modal: false,
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
.card-image1080 {
  transform: rotate(50deg);
  height: 160px;
  width: 160px;
}
</style>