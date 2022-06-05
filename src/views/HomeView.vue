<template>
<TypeEffect></TypeEffect>
<div class=" mt-2">
  <h1 class="text-2xl sm:text-3xl block">What is the <span class="text-sky-600 ">emoji code</span></h1>
  <div class="mt-3 flex gap-1 justify-items-center ">
    <input class="p-2 bg-slate-100 rounded-md ml-auto" type="text" placeholder="Unicode" v-model="unicode" @keyup.enter="check">
    <button class="bg-slate-100 rounded-md p-2 mr-auto border-solid border-slate-900 border-2" @click="check">Check</button>
  </div>
  <p class="text-transparent">https://unicode.org/emoji/charts/full-emoji-list.html</p>
</div>
<div class="bg-slate-100 rounded-md sm:p-5 w-fit text-center m-auto border-solid border-slate-900 border-2 p-2 sm:pr-32 sm:pl-32 flex gap-2 flex-col" v-show="q1">
  <h1>"Once upon a time there is a ..."</h1>
  <h1 class="text-xl block">คำใบ้ที่สอง</h1>
  <button class="bg-sky-100 rounded-md p-2 hover:bg-sky-200" @click="nextQ">Check here</button>
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
        this.unicode = "";
      } else {
        alert("Wrong");
        this.unicode = "";
      }
    },
    nextQ() {
      this.$router.push('/question2');
    }
  },
}
</script>