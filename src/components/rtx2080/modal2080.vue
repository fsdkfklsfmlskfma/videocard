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
          GeForce RTX 2080 — это видеокарта NVIDIA для энтузиастов, выпущенная
          20 сентября 2018 года.<br/><br/> Созданная на основе 12-нм техпроцесса и
          основанная на графическом процессоре TU104, в варианте TU104-400A-A1
          карта поддерживает DirectX 12. Окончательный. Это гарантирует, что все
          современные игры будут работать на GeForce RTX 2080.<br/><br/> Кроме того,
          возможность DirectX 12 Ultimate гарантирует поддержку аппаратной
          трассировки лучей, шейдинга с переменной скоростью и многого другого в
          будущих видеоиграх. Графический процессор TU104 представляет собой
          большой чип с площадью кристалла 545 мм² и 13 600 млн транзисторов.<br/><br/> В
          отличие от полностью разблокированной GeForce RTX 2080 SUPER, которая
          использует тот же графический процессор, но поддерживает все 3072
          шейдера, NVIDIA отключила некоторые блоки затенения на GeForce RTX
          2080, чтобы достичь целевого количества шейдеров продукта. Он имеет
          2944 модуля затенения, 184 модуля наложения текстур и 64 ROP.<br/><br/> Также
          включены 368 тензорных ядер, которые помогают повысить скорость
          приложений машинного обучения. Карта также имеет 46 ядер ускорения
          трассировки лучей. NVIDIA объединила 8 ГБ памяти GDDR6 с GeForce RTX
          2080, которые подключаются с помощью 256-битного интерфейса памяти.
          Графический процессор работает на частоте 1515 МГц, которую можно
          увеличить до 1710 МГц, память работает на частоте 1750 МГц (14 Гбит/с
          эффективно).<br/><br/> Будучи двухслотовой картой, NVIDIA GeForce RTX 2080
          получает питание от 1x 6-контактного + 1x 8-контактного разъема
          питания с максимальной потребляемой мощностью 215 Вт. Выходы дисплея
          включают: 1x HDMI 2.0, 3x DisplayPort 1.4a, 1x USB Type-C. GeForce RTX
          2080 подключается к остальной системе с помощью интерфейса PCI-Express
          3.0 x16. Размеры карты составляют 267 мм x 116 мм x 35 мм, и она имеет
          двухслотовое решение для охлаждения.<br/><br/> Его цена на старте составляла 2359,46 беларусских рублей.
        </p>
      </div>

      <div class="card-image2080RTX">
        <img src="./2080.png" alt="" />
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
.card-image2080RTX {
  transform: rotate(50deg);
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
