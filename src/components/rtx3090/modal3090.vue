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
          GeForce RTX 3090 — это видеокарта NVIDIA для энтузиастов, выпущенная 1
          сентября 2020 года.<br/><br/> Созданная на основе 8-нм техпроцесса и основанная
          на графическом процессоре GA102, в варианте GA102-300-A1 карта
          поддерживает DirectX 12. Окончательный. Это гарантирует, что все
          современные игры будут работать на GeForce RTX 3090. Кроме того,
          возможность DirectX 12 Ultimate гарантирует поддержку аппаратной
          трассировки лучей, шейдинга с переменной скоростью и многого другого в
          будущих видеоиграх.<br/><br/> Графический процессор GA102 представляет собой
          большой чип с площадью кристалла 628 мм² и 28 300 миллионами
          транзисторов. В отличие от полностью разблокированной GeForce RTX 3090
          Ti, которая использует тот же графический процессор, но поддерживает
          все 10752 шейдера, NVIDIA отключила некоторые блоки затенения на
          GeForce RTX 3090, чтобы достичь целевого количества шейдеров продукта.
          Он имеет 10496 блоков затенения, 328 блоков наложения текстур и 112
          ROP. Также включены 328 тензорных ядер, которые помогают повысить
          скорость приложений машинного обучения.<br/><br/> Карта также имеет 82 ядра
          ускорения трассировки лучей. NVIDIA объединила 24 ГБ памяти GDDR6X с
          GeForce RTX 3090, которые подключаются с помощью 384-битного
          интерфейса памяти. Графический процессор работает на частоте 1395 МГц,
          которая может быть увеличена до 1695 МГц, память работает на частоте
          1219 МГц (эффективная 19,5 Гбит/с).<br/><br/> Будучи картой с тремя слотами,
          NVIDIA GeForce RTX 3090 получает питание от 1x 12-контактного разъема
          питания с максимальной потребляемой мощностью 350 Вт. Выходы дисплея
          включают: 1x HDMI 2.1, 3x DisplayPort 1.4a. GeForce RTX 3090
          подключается к остальной системе с помощью интерфейса PCI-Express 4.0
          x16. Размеры карты составляют 336 мм x 140 мм x 61 мм, и она оснащена
          системой охлаждения с тремя слотами.<br/><br/> Его цена на момент запуска
          составляла 7754 Беларуских рублей.
        </p>
      </div>

      <div class="card-image3090RTX">
        <img src="./3090.png" alt="" />
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
.card-image3090RTX {
  transform: rotate(222deg);
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
