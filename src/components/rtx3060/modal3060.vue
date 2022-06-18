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
          GeForce RTX 3060 — это видеокарта высокопроизводительного сегмента от
          NVIDIA, выпущенная 12 января 2021 года.<br/><br/> Созданная на основе 8-нм
          техпроцесса и основанная на графическом процессоре GA106, в варианте
          GA106-300-A1 карта поддерживает DirectX 12.<br/><br/> Окончательный. Это
          гарантирует, что все современные игры будут работать на GeForce RTX
          3060. Кроме того, возможность DirectX 12 Ultimate гарантирует
          поддержку аппаратной трассировки лучей, шейдинга с переменной
          скоростью и многого другого в будущих видеоиграх. Графический
          процессор GA106 представляет собой чип среднего размера с площадью
          кристалла 276 мм² и 12 000 миллионов транзисторов.<br/><br/> Он имеет 3584 блока
          затенения, 112 блоков наложения текстур и 48 ROP. Также включены 112
          тензорных ядер, которые помогают повысить скорость приложений
          машинного обучения. Карта также имеет 28 ядер ускорения трассировки
          лучей.<br/><br/> NVIDIA объединила 12 ГБ памяти GDDR6 с GeForce RTX 3060,
          которые подключаются с помощью 192-битного интерфейса памяти.
          Графический процессор работает на частоте 1320 МГц, которую можно
          увеличить до 1777 МГц, память работает на частоте 1875 МГц (15 Гбит/с
          эффективно). Будучи двухслотовой картой, NVIDIA GeForce RTX 3060
          получает питание от 1x 12-контактного разъема питания с максимальной
          потребляемой мощностью 170 Вт.<br/><br/> Выходы дисплея включают: 1x HDMI 2.1,
          3x DisplayPort 1.4a. GeForce RTX 3060 подключается к остальной системе
          с помощью интерфейса PCI-Express 4.0 x16. Карта имеет длину 242 мм,
          ширину 112 мм и имеет двухслотовое решение для охлаждения. <br/><br/>Его цена на
          момент запуска составляла 1 979,57 беларусских рублей.
        </p>
      </div>

      <div class="card-image3060GTX">
        <img src="./3060.png" alt="" />
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
.card-image3060GTX {
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
