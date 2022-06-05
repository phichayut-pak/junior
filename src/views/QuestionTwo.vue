<template>
    <h1 class="text-3xl">กําหนดสมการ <span class="text-sky-600 font-black">x<sup>4</sup> - 13x<sup>3</sup> + 28x<sup>2</sup> - 23x + 6 = 0</span> ผลบวกของคําตอบของสมการคืออะไร</h1>
    <div class="mt-3 flex gap-1 justify-items-center ">
        <input class="p-2 bg-slate-100 rounded-md ml-auto w-3/12" type="text" placeholder="Answer" v-model="Answer" @keyup.enter="check">
        <button class="bg-slate-100 rounded-md p-2 mr-auto border-solid border-slate-900 border-2" @click="check">Check</button>
    </div>
    <div class="bg-slate-100 rounded-md sm:p-5 w-fit text-center m-auto border-solid border-slate-900 border-2 p-2 sm:pr-32 sm:pl-32 flex gap-2 flex-col" v-show="q2">
        <h1></h1>
        <h1 class="text-xl block">คำใบ้ต่อไปคือ</h1>
        <button class="bg-sky-100 rounded-md p-2 hover:bg-sky-200" @click="nextQ">coming soon</button>
    </div>
</template>

<script>
export default {
  data() {
    return {
      Answer: "",
      q2: false,
    };
  },
  methods: {
    check() {
      if (this.unicode === "U+1F44A") {
        this.q2 = true;
        this.Answer = "";
      } else {
        alert("Wrong");
        this.Answer = "";
      }
    },
    nextQ() {
      this.$router.push('/question2');
    }
  },
}
</script>

<style>

</style>