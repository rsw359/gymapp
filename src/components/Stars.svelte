<div class="flex items-center justify-center gap-2 text-base">
  <p>4.6</p>
  {#each [0,1,2,3,4] as index }
   <div class="relative grid place-items-center">
    <i class="opacity-0 fa-solid fa-star"></i>
    <div class={"absolute top-0 left-0 grid place-items-center " + (index === 4 ? "w-[60%] overflow-hidden" : " " )}>
    <i class="fa-solid fa-star text-amber-400"></i>
    </div>
  </div>
  
  {/each}
  <p>500+</p>
</div>