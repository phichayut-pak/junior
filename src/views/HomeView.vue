<template>
<TypeEffect></TypeEffect>
<div class="w-full mt-4">
  <h1 class="text-6xl block">What is the <span class="text-sky-600">emoji code</span></h1>
  <div class="mt-3 flex gap-1 justify-items-center ">
    <input class="p-2 bg-slate-100 rounded-md ml-auto" type="text" placeholder="Unicode" v-model="unicode" @keyup.enter="check">
    <button class="bg-slate-100 rounded-md p-2 mr-auto border-solid border-gray-900 border-2" @click="check">Check</button>
  </div>
  <p class="text-transparent">https://unicode.org/emoji/charts/full-emoji-list.html</p>
  <div class="bg-slate-100 rounded-md p-5" v-show="q1">
    <h1>คำใบ้ต่อไปจะมาในวันพรุ่งนี้</h1>
  </div>
</div>
</template>

<script>
// @ is an alias to /src
import TypeEffect from "@/components/TypeEffect.vue";

export default {
  components: {
    // eslint-disable-next-line vue/no-unused-components
    TypeEffect,
  },
  data() {
    return {
      unicode: "",
      q1: false,
    };
  },
  methods: {
    check() {
    if (this.unicode === "U+1F44A") {
      this.q1 = true;
    } else {
      alert("Wrong");
    }
    }

  },
}
</script>
