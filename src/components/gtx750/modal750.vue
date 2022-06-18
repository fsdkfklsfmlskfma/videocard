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
          GeForce GTX 750 — это видеокарта среднего класса от NVIDIA, выпущенная
          18 февраля 2014 года.<br/><br/>Созданная по 28-нм техпроцессу и основанная на
          графическом процессоре GM107, в варианте GM107-300-A2 карта
          поддерживает DirectX 12. <br/><br/>Графический процессор GM107 представляет
          собой чип среднего размера с площадью кристалла 148 мм² и 1 870
          миллионами транзисторов. В отличие от полностью разблокированной
          GeForce GTX 750 Ti, которая использует тот же графический процессор,
          но поддерживает все 640 шейдеров, NVIDIA отключила некоторые шейдерные
          блоки на GeForce GTX 750, чтобы достичь целевого количества шейдеров
          продукта. Он имеет 512 блоков затенения, 32 блока наложения текстур и
          16 ROP.<br/><br/> NVIDIA объединила 1024 МБ памяти GDDR5 с GeForce GTX 750,
          которые подключаются через 128-битный интерфейс памяти.<br/><br/> Графический
          процессор работает на частоте 1020 МГц, которую можно увеличить до
          1085 МГц, память работает на частоте 1253 МГц (эффективно 5 Гбит/с).
          Будучи однослотовой картой, NVIDIA GeForce GTX 750 не требует
          дополнительного разъема питания, ее потребляемая мощность составляет
          максимум 55 Вт. <br/><br/>Выходы дисплея включают: 2x DVI, 1x mini-HDMI 2.0.
          GeForce GTX 750 подключается к остальной системе с помощью интерфейса
          PCI-Express 3.0 x16. Карта имеет длину 145 мм и имеет однослотовое
          решение для охлаждения.<br/><br/> Его цена на момент запуска составляла 671,72 беларусских рублей.
        </p>


      </div>
      <div class="card-image750gtx">
        <img src="./750.png" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
import { ref, reactive, defineProps, onMounted } from "vue";
import gsap from "gsap";

export default {
  props: {
    show: Boolean,
  },

  setup(props) {
    const number = ref(0);
    const tweened = reactive({
      number: 0,
    });
    let show = ref(props.show);

    gsap.to(tweened, { duration: 0.5, number: Number(550) || 0 });

    onMounted(() => {
      console.log(props.show);
    });

    return {
      number,
      tweened,
    };
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
  overflow: scroll;
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
.card-image750gtx {
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
