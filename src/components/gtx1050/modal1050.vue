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
          GeForce GTX 1050 — это видеокарта среднего класса от NVIDIA,
          выпущенная 25 октября 2016 года.<br/><br/> Созданная на основе 14-нм техпроцесса
          и основанная на графическом процессоре GP107, в варианте GP107-300-A1
          карта поддерживает DirectX 12. Это гарантирует, что все современные
          игры будут работать на GeForce GTX 1050. <br/><br/>Графический процессор GP107
          представляет собой чип среднего размера с площадью кристалла 132 мм² и
          3 300 миллионами транзисторов. В отличие от полностью разблокированной
          GeForce GTX 1050 Ti, которая использует тот же графический процессор,
          но поддерживает все 768 шейдеров, NVIDIA отключила некоторые шейдерные
          блоки на GeForce GTX 1050, чтобы достичь целевого количества шейдеров
          продукта. Он имеет 640 блоков затенения, 40 блоков наложения текстур и
          32 ROP.<br/><br/> NVIDIA объединила 2048 МБ памяти GDDR5 с GeForce GTX 1050,
          которые подключаются через 128-битный интерфейс памяти. Графический
          процессор работает на частоте 1354 МГц, которая может быть увеличена
          до 1455 МГц, память работает на частоте 1752 МГц (эффективно 7
          Гбит/с). Будучи двухслотовой картой, NVIDIA GeForce GTX 1050 не
          требует дополнительного разъема питания, ее потребляемая мощность
          составляет максимум 75 Вт. <br/><br/>Выходы дисплея включают: 1x DVI, 1x HDMI
          2.0, 1x DisplayPort 1.4a. GeForce GTX 1050 подключается к остальной
          системе с помощью интерфейса PCI-Express 3.0 x16. Карта имеет длину
          145 мм, ширину 111 мм и имеет двухслотовое решение для охлаждения.<br/><br/> Его
          цена на момент запуска составляла 367,93 беларусских рублей.
        </p>
      </div>

      <div class="card-image1050gtx">
        <!-- ! ИЗМЕНИТЬ КАРТИНКУ -->
        <img src="./1050.png" alt="" />
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
.card-image1050gtx {
  transform: rotate(35deg);
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
