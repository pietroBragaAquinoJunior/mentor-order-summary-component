<template>
  <div class="h-[100vh] bg-[url('images/pattern-background-mobile.svg')] bg-no-repeat bg-[hsl(225,100%,94%)] flex justify-center items-center xs:bg-[url('images/pattern-background-desktop.svg')]">
    <div class="flex flex-col w-[325px] h-[560px] bg-white rounded-3xl md:w-[450px] md:h-[700px]">
      <img class="rounded-t-2xl flex-0.5" src="/images/illustration-hero.svg" alt="Illustration Hero">
      <div class="p-6 flex justify-around flex-col items-center h-full md:p-12">
        <h1 class="text-2xl font-[900] text-[hsl(223,47%,23%)]  md:text-[30px] md:text-3xl">
          Order Summary
        </h1>
        <p class="text-center text-md text-[hsl(224,23%,55%)] md:text-base ">
          You can now listen to millions of songs, audiobooks, and podcasts on any
          device anywhere you like!
        </p>
        <div class="w-full flex justify-between bg-[hsl(225,100%,98%)] rounded-lg  items-center p-4 md:p-6">
          <div class="flex">
            <div class="rounded-full bg-[hsl(225,100%,94%)] w-[45px] h-[45px]">
              <img src="/images/icon-music.svg" alt="Icon Music">
            </div>
            <div class="ml-[30px]">
              <h1 class="font-[900] text-sm md:text-base">
                Annual Plan
              </h1>
              <p class="text-[hsl(224,23%,55%)] text-sm md:text-base">
                $59.99/year
              </p>
            </div>
          </div>

          <div>
            <p class="text-sm text-[hsl(245,75%,52%)] border-b-[1px] border-b-[hsl(245,75%,52%)] font-[900] leading-[12px] cursor-pointer hover:text-[hsla(245,75%,52%,0.8)] md:text-md">
              Change
            </p>
          </div>
        </div>

        <button class="w-full p-3 bg-[hsl(245,75%,52%)] rounded-xl text-white font-[900] text-md shadow-xl  hover:bg-[hsla(245,75%,52%,0.8)] cursor-pointer md:p-4 md:text-base">
          Proceed to Payment
        </button>

        <button class="font-[900] text-[hsl(224,23%,55%)] text-md cursor-pointer hover:text-[hsl(223,47%,23%)] md:text-base">
          Cancel Order
        </button>
      </div>
    </div>
  </div>
</template>

<script>
// Descobrir se é mobile ou não para alterar a imagem de fundo.
const isMobile = ref(false)
const checkMediaQuery = () => {
  isMobile.value = window.matchMedia('(max-width: 375px)').matches
}
onMounted(() => {
  checkMediaQuery()
  window.addEventListener('resize', checkMediaQuery)
})
onBeforeUnmount(() => {
  window.removeEventListener('resize', checkMediaQuery)
})
</script>
