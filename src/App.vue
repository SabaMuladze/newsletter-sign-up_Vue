
<template>
  <div
    class="w-full h-screen flex flex-col bg-white max-md:pb-6 justify-between  md:w-fit lg:flex-row-reverse md:rounded-lg lg:rounded-[36px] lg:w-[930px] lg:h-[630px] lg:pr-5">
    <div class="img h-[285px] bg-cover bg-no-repeat md:rounded-lg lg:w-[50%]"></div>
    <div class="px-6 lg:px-16 md:py-5 lg:py-24">
      <div class="flex flex-col gap-6">
        <h1 class="mt-6 text-4xl md:text-[56px]">Stay updated!</h1>
        <p class="mb-6">Join 60,000+ product managers receiving monthly updates on:</p>
      </div>

      <div class="flex py-[5px]"><img class=" self-start mr-4" src="./assets/images/icon-success.svg" alt="" height="21"
          width="21">
        <p>Product discovery and building what matters</p>
      </div>
      <div class="flex py-[5px]"><img class=" self-start mr-4" src="./assets/images/icon-success.svg" alt="" height="21"
          width="21">
        <p>Measuring to ensure updates are a success</p>
      </div>
      <div class="flex py-[5px]"><img class=" self-start mr-4" src="./assets/images/icon-success.svg" alt="" height="21"
          width="21">
        <p>And much more!</p>
      </div>
      <div class="mt-10">
        <div class="flex justify-between"><label for="email" class="font-bold">Email Adress</label>
          <p v-if="warning" class="text-[#FF6155]">Valid email required</p>
        </div>
        <div class=" border-solid border-[1px] border-[rgba(25, 24, 43, 0.25)] rounded-lg"><input v-model="email"
            v-on:change="inptColor" :style="inputStyles" class="px-6 py-4 w-full rounded-lg outline-none" name="email"
            type="email" placeholder="email@company.com">
        </div>

        <button @click="validateEmail"
          class="bg-[#242742] text-white font-bold w-full py-5 px-8 rounded-lg mt-6 hover:bg-gradient-to-tl from-[#FF6A3A] to-[#FF527B] shadow-xl">Subscribe
          to
          monthly
          newsletter</button>
      </div>
    </div>

  </div>
  <div v-if="showSection" class="w-full h-screen bg-[#36384D] absolute top-0">

  </div>
  <div v-if="showSection"
    class="w-full h-screen bg-white absolute top-0 flex flex-col justify-between px-6 pb-6 md:w-fit lg:w-[504px] lg:h-[520px] lg:top-auto lg:rounded-[36px] lg:px-16 lg:pb-16">
    <div class="mt-[150px] lg:mt-[48px]">
      <img src="./assets/images/icon-success.svg" height="64" width="64" alt="">
      <h1 class="mt-10 text-4xl mb-6 md:text-[56px] leading-[100%]">Thanks for subscribing!</h1>
      <p class=" leading-[150%]">A confirmation email has been sent to <span class="font-bold">{{ email }}</span>
        Please open
        it and
        click the button inside to confirm
        your subscription</p>
    </div>
    <button @click="dismiss"
      class='bg-[#242742] text-white font-bold w-full py-5 px-8 rounded-lg mt-6 hover:bg-gradient-to-tl from-[#FF6A3A] to-[#FF527B] shadow-xl'>Dismiss
      message</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showSection: false,
      btnhover: 'bg-gradient-to-tl from-[#FF6A3A] to-[#FF527B]',
      email: '',
      warning: false,

    }
  },
  methods: {
    send() {
      this.showSection = true
    },
    dismiss() {
      this.showSection = false
    },
    validateEmail() {
      if (this.emailValidate(this.email)) {
        this.warning = false
        this.send()
      } else {
        this.warning = true
      }
    },
    emailValidate(email) {
      const emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$/;
      return emailPattern.test(email);
    },
    inptColor(event) {
      let input = event.target;
    }

  },
  computed: {
    inputStyles() {
      return {
        background: this.warning == true ? 'rgba(255, 97, 85, 0.15)' : '#fff',
      }
    }
  }
}

</script>

<style scoped>
.img {
  background: url(./assets/images/illustration-sign-up-mobile.svg);
  background-size: 100%;
  background-position: center;
  background-repeat: no-repeat;

}



p {
  font-size: 16px;
  font-weight: 400;
}

h1 {
  font-weight: 700;
}

@media (min-width:768px) {
  .img {
    background: url(./assets/images/illustration-sign-up-desktop.svg);
    background-size: 100%;
    background-position: center;
    background-repeat: no-repeat;
    height: 100%;
  }
}
</style>
