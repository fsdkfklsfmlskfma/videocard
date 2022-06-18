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
          GeForce GTX 1080 — это высокопроизводительная видеокарта от NVIDIA,
          выпущенная 27 мая 2016 года.<br/><br/> Созданная по 16-нм техпроцессу и
          основанная на графическом процессоре GP104, в варианте GP104-400-A1
          карта поддерживает DirectX 12. Это гарантирует, что все современные
          игры будут работать на GeForce GTX 1080.<br/><br/>  Графический процессор GP104
          представляет собой большой чип с площадью кристалла 314 мм² и 7 200
          миллионами транзисторов. Он имеет 2560 блоков затенения, 160 блоков
          наложения текстур и 64 ROP. NVIDIA объединила 8 ГБ памяти GDDR5X с
          GeForce GTX 1080, которые подключаются с помощью 256-битного
          интерфейса памяти. <br/><br/>Графический процессор работает на частоте 1607 МГц,
          которую можно увеличить до 1733 МГц, память работает на частоте 1251
          МГц (10 Гбит/с эффективно). Будучи двухслотовой картой, NVIDIA GeForce
          GTX 1080 получает питание от 1x 8-контактного разъема питания с
          максимальной потребляемой мощностью 180 Вт.<br/><br/> Выходы дисплея включают:
          1x DVI, 1x HDMI 2.0, 3x DisplayPort 1.4a. GeForce GTX 1080
          подключается к остальной системе с помощью интерфейса PCI-Express 3.0
          x16. Размеры карты составляют 267 мм x 112 мм x 40 мм, и она имеет
          двухслотовое решение для охлаждения.<br/><br/> Его цена на старте составляла 2021,91 беларусских рублей.
        </p>
      </div>

      <div class="card-image1080gtx">
        <img src="./1080.png" alt="" />
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
.card-image1080gtx {
  margin-right: 400px;
  margin-bottom: 400px;
  transform: rotate(50deg);
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
