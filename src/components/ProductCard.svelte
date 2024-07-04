  <script>
    export let index
    export let productFeature
  </script> 

<div class="relative grid grid-cols-1 gap-10 text-base md:grid-cols-2 md:gap:14 lg:gap-20">
  
  　<div class={"flex flex-col gap-8 md:gap-10 pt-8 sm:pt-10" + (index % 2 === 1 ? ' md:order-2 ' : '' )}> 
    <h4 class="text-2xl sm:text-3xl md:text-4xl max-w-[1000px] w-full font-medium relative pr-10 after:absolute after:top-full after:left-0 after:w-1/5 after:h-1.5 after:mt-1 after:bg-slate-900">
    <slot/>
    </h4>
    <p>{productFeature.description}</p>
    <div class="flex flex-col gap-3 ">
      {#each productFeature.featureList as listItem }
        <div class="flex items-center gap-2">
          <div  class="grid place-items-center px-1.5 text-xs sm:text-sm aspect-square rounded-full border-[1.5px] bg-white border-solid border-green-300">
            <i class="text-green-400 fa-solid fa-bolt"></i>
          </div>
          <p>{listItem}</p>
        </div>
      {/each}
    </div>
    <div class="flex items-center">
      <button class="mr-auto font-semibold specialBtnDark">
        <p>Try free today &rarr;</p>
      </button>
    </div>
  </div>
  <div class={"flex flex-col dropShadow overflow-hidden rounded-b-lg"}>
    <div class="flex items-center h-8 gap-2 px-3 bg-white rounded-t-xl sm:h-10 opacity-60">
      {#each [1,2,3] as i }
      <div class="rounded-full aspect-square w-2.5 sm:w-3 bg-indigo-300"/>
      {/each }
    </div>
    <div class="flex flex-col flex-1 gap-4 bg-white">
      <img src={productFeature.imgUrl} alt="">
    </div>
  </div>
</div> 