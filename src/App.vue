
<template>
  <div class="w-full min-h-screen flex flex-col bg-white md:w-fit">
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
</template>

<script>

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
