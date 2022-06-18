<template>
  <div id="modal-container" v-if="show">
    <div class="controls">
      <button class="modal-close" @click="$emit('close')">
        <img src="../back.svg" />
      </button>
      <img src="../nvidia.png" class="nvidia" />
    </div>

    <div id="modal-mask">
      <div class="card-description">
        <p>
          <!-- ИЗМЕНИТЬ ТЕКСТ -->
          GeForce GTX 970 — это видеокарта высокопроизводительного сегмента от
          NVIDIA, выпущенная 19 сентября 2014 года.<br/><br/> Созданная на основе 28-нм
          техпроцесса и основанная на графическом процессоре GM204, в варианте
          GM204-200-A1 карта поддерживает DirectX 12. Это гарантирует, что все
          современные игры будут работать на GeForce GTX 970.<br/><br/> Графический
          процессор GM204 представляет собой большой чип с площадью кристалла
          398 мм² и 5 200 миллионами транзисторов.<br/><br/> В отличие от полностью
          разблокированной GeForce GTX 980, которая использует тот же
          графический процессор, но поддерживает все 2048 шейдеров, NVIDIA
          отключила некоторые шейдерные блоки на GeForce GTX 970, чтобы достичь
          целевого количества шейдеров продукта. Он имеет 1664 модуля затенения,
          104 модуля наложения текстур и 56 ROP.<br/><br/> NVIDIA объединила 4 ГБ памяти
          GDDR5 с GeForce GTX 970, которые подключаются с помощью 256-битного
          интерфейса памяти. Графический процессор работает на частоте 1050 МГц,
          которую можно увеличить до 1178 МГц, память работает на частоте 1753
          МГц (эффективно 7 Гбит/с). Будучи двухслотовой картой, NVIDIA GeForce
          GTX 970 питается от двух 6-контактных разъемов питания с максимальной
          потребляемой мощностью 148 Вт.<br/><br/> Выходы дисплея включают: 1x DVI, 1x
          HDMI 2.0, 3x DisplayPort 1.4a. GeForce GTX 970 подключается к
          остальной системе с помощью интерфейса PCI-Express 3.0 x16. Размеры
          карты составляют 267 мм x 111 мм x 40 мм, и она имеет двухслотовое
          решение для охлаждения. <br/><br/>Его цена на момент запуска составляла 1110,53 беларусских рублей.
        </p>
      </div>

      <div class="card-image970gtx">
        <!-- ! ИЗМЕНИТЬ КАРТИНКУ -->

        <img src="./970.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    show: Boolean,
  },
};
</script>

<style>
#modal-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;

  z-index: 9998;

  background: linear-gradient(180deg, #000000 42.19%, rgb(13, 117, 11) 100%);
}
.card-description {
  color: #fff;
  text-align: left;
  width: 700px;
  font-size: 20px;

  margin-left: 3rem;
}
.card-image970gtx {
  transform: rotate(30deg);
  margin-right: 20rem;
  margin-bottom: 20rem;
}
#modal-mask {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.modal-close {
  background: none;
  border: none;
}
.controls {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
}
.nvidia {
  height: 80px;
}
</style>
