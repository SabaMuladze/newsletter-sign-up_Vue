
<template>
  <div class="w-full min-h-screen flex flex-col bg-white hidden md:w-fit">
    <div class="img h-[285px] bg-cover bg-no-repeat"></div>
    <div class="px-6">
      <div class="flex flex-col gap-6">
        <h1 class="mt-6 text-4xl">Stay updated!</h1>
        <p class="mb-6">Join 60,000+ product managers receiving monthly updates on:</p>
      </div>

      <div class="flex "><img class=" self-start mr-4" src="./assets/images/icon-success.svg" alt="" height="21"
          width="21">
        <p>Product discovery and building what matters</p>
      </div>
      <div class="flex "><img class=" self-start mr-4" src="./assets/images/icon-success.svg" alt="" height="21"
          width="21">
        <p>Measuring to ensure updates are a success</p>
      </div>
      <div class="flex "><img class=" self-start mr-4" src="./assets/images/icon-success.svg" alt="" height="21"
          width="21">
        <p>And much more!</p>
      </div>
    </div>
    <div class="px-6 mt-10">
      <label for="email" class="font-bold">Email Adress</label>
      <div class=" border-solid border-[1px] border-[rgba(25, 24, 43, 0.25)] rounded-lg"><input
          class="px-6 py-4 w-full rounded-lg h-[]" name="email" type="email">
      </div>

      <button class="bg-[#242742] text-white font-bold w-full py-5 px-8 rounded-lg mt-6">Subscribe to monthly
        newsletter</button>
    </div>
  </div>
  <div class="w-full min-h-screen bg-white absolute flex flex-col justify-between px-6 pb-10 md:w-fit">
    <div class="mt-[150px]">
      <img src="./assets/images/icon-success.svg" height="64" width="64" alt="">
      <h1 class="mt-10 text-4xl mb-6">Thanks for subscribing!</h1>
      <p class=" leading-[150%]">A confirmation email has been sent to <span
          class="font-bold">ash@loremcompany.com.</span> Please open
        it and
        click the button inside to confirm
        your subscription</p>
    </div>
    <button class='bg-[#242742] text-white font-bold w-full py-5 px-8 rounded-lg mt-6'>Dismiss message</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showSection: false,
    }
  },
  methods: {
    send() {
      this.showSection == false ? this.showSection = true : this.showSection == false
    }
  },
  computed: {

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

h1,
h2,
p {
  color: #242742;
}

p {
  font-size: 16px;
  font-weight: 400;
}

h1 {
  font-weight: 700;
}

@media (min-width:768px) {
  img {
    background: url(./assets/images/illustration-sign-up-desktop.svg);
  }
}
</style>
