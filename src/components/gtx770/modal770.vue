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
          GeForce GTX 770 — это высококлассная видеокарта от NVIDIA, выпущенная
          30 мая 2013 года.<br/><br/> Созданная по 28-нм техпроцессу и основанная на
          графическом процессоре GK104, в варианте GK104-425-A2 карта
          поддерживает DirectX 12.<br/><br/> Графический процессор
          GK104 представляет собой чип среднего размера с площадью кристалла 294
          мм² и 3 540 миллионами транзисторов. <br/><br/> Он имеет 1536 блоков затенения,
          128 блоков наложения текстур и 32 ROP. NVIDIA объединила 2048 МБ
          памяти GDDR5 с GeForce GTX 770, которые подключаются с помощью
          256-битного интерфейса памяти. Графический процессор работает на
          частоте 1046 МГц, которую можно увеличить до 1085 МГц, память работает
          на частоте 1753 МГц (эффективно 7 Гбит/с).<br/><br/> Будучи двухслотовой картой,
          NVIDIA GeForce GTX 770 получает питание от 1x 6-контактного + 1x
          8-контактного разъема питания с максимальной потребляемой мощностью
          230 Вт. Выходы дисплея включают: 2x DVI, 1x HDMI 1.4a, 1x DisplayPort
          1.2. GeForce GTX 770 подключается к остальной системе с помощью
          интерфейса PCI-Express 3.0 x16.<br/><br/>  Размеры карты составляют 267 мм x 111
          мм x 38 мм, и она имеет двухслотовое решение для охлаждения.<br/><br/>  Его цена
          на старте составляла 1346,82 беларусских рублей.
        </p>
      </div>

      <div class="card-image770gtx">
        <img src="./770.png" alt="" />
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
.card-image770gtx {
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
