<template>
  <div class="root">
    <div class="main-card" @click="show750Modal = true">
        <img class="card-image750" src="./750.png" />

      <div class="image-overlay image-overlay__primary">
        <p class="image-title">Информация</p>        
      </div>

      <h1 class="card-header">GTX 750</h1>

      <p class="card-text">
      GeForce GTX 750 — видеокарта среднего класса от NVIDIA, выпущенная 18 февраля 2014 года.
      </p>
    </div>

    <Teleport to="body">
      <Modal 
        :show="show750Modal"
        @close="show750Modal = false"
      />
    </Teleport>
  </div>
</template>

<script>
import Modal from './modal750.vue'

  export default {
    components: {
      Modal,
    },

    data: () => ({
      show750Modal: false,
    })
  };

</script>

<style>
.main-card {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

  position: relative;

  color: #00ff29;

  background-color: black;
  box-shadow: 10px 10px 10px rgba(24, 24, 24, 0.379);

  margin-top: 30px;
  margin-right: 62px;

  padding: 10px;

  width: 220px;
  height: 350px;
}
    .main-card:hover {
        content: attr(data-title); 
        transition: 0.5s ease-in-out;
        background: black;
        font-size: 16px;  
} 
/* Анимация текста */
.image-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.6);
    color: #ffffff;

   font-family: 'Source Sans Pro', sans-serif;
    font-weight: bold;
    font-size: 20px;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    opacity: 0;
    transition: opacity 0.25s;
}

.image-title {
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgba(45, 219, 2, 0.655);
  width: 100%;
  height: 50px;
  text-align: center;
}

.image-overlay:hover > * {
   transform: translateY(0);
}
.image-overlay:hover {
    opacity: 1;
}
/* Анимация текста */




.text-visible {
  width: 100%;
  border: 1px solid red;
  text-align: center;
}

.card-text {
  color: #fff;
  font-weight: bold;
  font-size: 18px;
}


.card-image750 {
  position: relative;
  transform: rotate(30deg);
  height: 160px;
  width: 160px;
}



.emerging-text {
  color: #fff;
  font-weight: bold;
  font-size: 18px;
  border: #fff solid 1px;
  position: absolute;
  top: 600px;
  /* opacity: 0; */

}
/* .emerging-text:hover {
  opacity: 1;
  z-index: 9998;
} */

.emerhing-text {
  top: 0;
  left: 100% ;
}
</style>