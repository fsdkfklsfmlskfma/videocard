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
          GeForce GTX 1060 6 ГБ — это видеокарта высокопроизводительного
          сегмента от NVIDIA, выпущенная 19 июля 2016 года. <br/><br/>Созданная на основе
          16-нм техпроцесса и основанная на графическом процессоре GP106, в
          варианте GP106-400-A1 карта поддерживает DirectX 12. Это гарантирует,
          что все современные игры будут работать на GeForce GTX 1060 6 ГБ.
          Графический процессор GP106 представляет собой чип среднего размера с
          площадью кристалла 200 мм² и 4 400 миллионами транзисторов. <br/><br/>Он имеет
          1280 блоков затенения, 80 блоков наложения текстур и 48 ROP. NVIDIA
          объединила 6 ГБ памяти GDDR5 с GeForce GTX 1060 6 ГБ, которые
          подключаются с помощью 192-битного интерфейса памяти.<br/><br/> Графический
          процессор работает на частоте 1506 МГц, которую можно увеличить до
          1709 МГц, память работает на частоте 2002 МГц (эффективно 8 Гбит/с).
          Будучи двухслотовой картой, NVIDIA GeForce GTX 1060 6 ГБ получает
          питание от 1x 6-контактного разъема питания с максимальной
          потребляемой мощностью 120 Вт. Выходы дисплея включают: 1x DVI, 1x
          HDMI 2.0, 3x DisplayPort 1.4a.<br/><br/> GeForce GTX 1060 6 ГБ подключается к
          остальной системе по интерфейсу PCI-Express 3.0 x16. Карта имеет длину
          250 мм, ширину 111 мм и имеет двухслотовое решение для охлаждения.<br/><br/> Его
          цена на старте составляла 1009,27 беларусских рублей.
        </p>
      </div>

      <div class="card-image1060gtx">
        <img src="./1060.png" alt="" />
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
.card-image1060gtx {
  transform: rotate(20deg);
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
