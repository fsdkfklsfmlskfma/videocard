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
          GeForce GTX 1070 Ti — это высокопроизводительная видеокарта от NVIDIA,
          выпущенная 2 ноября 2017 года. <br/><br/>Созданная на основе 16-нм техпроцесса и
          основанная на графическом процессоре GP104, в варианте GP104-300-A1
          карта поддерживает DirectX. 12. Это гарантирует, что все современные
          игры будут работать на GeForce GTX 1070 Ti. <br/><br/>Графический процессор
          GP104 представляет собой большой чип с площадью кристалла 314 мм² и 7
          200 миллионами транзисторов. В отличие от полностью разблокированной
          GeForce GTX 1080, которая использует тот же графический процессор, но
          поддерживает все 2560 шейдеров, NVIDIA отключила некоторые блоки
          обработки теней на GeForce GTX 1070 Ti, чтобы достичь целевого
          количества шейдеров продукта. Он имеет 2432 модуля затенения, 152
          модуля наложения текстур и 64 ROP.<br/><br/> NVIDIA объединила 8 ГБ памяти GDDR5
          с GeForce GTX 1070 Ti, которые подключаются с помощью 256-битного
          интерфейса памяти. Графический процессор работает на частоте 1607 МГц,
          которую можно увеличить до 1683 МГц, память работает на частоте 2002
          МГц (эффективно 8 Гбит/с).<br/><br/> Будучи   двухслотовой картой, NVIDIA GeForce
          GTX 1070 Ti получает питание от 1x 8-контактного разъема питания с
          максимальной потребляемой мощностью 180 Вт.<br/><br/> Выходы дисплея включают:
          1x DVI, 1x HDMI 2.0, 3x DisplayPort 1.4a. GeForce GTX 1070 Ti
          подключается к остальной системе с помощью интерфейса PCI-Express 3.0
          x16. Размеры карты составляют 267 мм x 112 мм x 40 мм, и она имеет
          двухслотовое решение для охлаждения.<br/><br/> Его цена на старте составляла 1346,82 беларусских рублей.
        </p>
      </div>

      <div class="card-image1070ti">
        <img src="./1070ti.png" />
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
.card-image1070ti {
  transform: rotate(10deg);
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
