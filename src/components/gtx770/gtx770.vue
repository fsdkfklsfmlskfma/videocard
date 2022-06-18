<template>
  <div class="root">
    <div class="main-card" @click="show770Modal = true">
      <img class="card-image770" src="./770.png" />
            <div class="image-overlay image-overlay__primary">
        <p class="image-title">Информация</p>        
      </div>
      <h1 class="card-header">GTX 770</h1>

      <p class="card-text">
       GeForce GTX 770 — это высокопроизводительная видеокарта от NVIDIA, выпущенная 30 мая 2013 года. 
      </p>
    </div>

    <Teleport to="body">
      <Modal 
        :show="show770Modal"
        @close="show770Modal = false"
      />
    </Teleport>
  </div>
</template>

<script>
import Modal from './modal770.vue'

export default {
  components: {
    Modal,
  },

  data: () => ({
    show770Modal: false,
  })
};
</script>

<style>
.main-card {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

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
.card-image770 {
  height: 160px;
  width: 160;
}
</style>