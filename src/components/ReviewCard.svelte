<script>
  export let reviewItem;
  export let left;
  export let index;
</script>

<div
  class={"flex flex-col gap-2 w-full max-w-[500px] mx-auto relative " +
      (left
          ? index % 2 === 1
              ? "hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden"
              : " "
          : index % 2 === 0
            ? "hidden md:flex opacity-0 pointer-events-none max-h-[40px] overflow-hidden"
            : " ")}
>
  <div class="relative flex">
      <div
          class={"absolute reounded-full bg-white aspect-square hidden md:grid place-items-center h-4 top-0 " +
              (index % 2 === 0
                  ? " right-0 -mr-8 translate-x-1/2"
                  : " left-0 -ml-8 -translate-x-1/2")}
      >
          <div
              class="h-2 rounded-full bg-slate-950 aspect-square"
          />
      </div>
      <div class="flex items-center gap-2">
          <i class="fa-solid fa-user" />
          <h3 class="text-lg sm:text-xl md:text-2xl">
              {reviewItem.name}
          </h3>
      </div>
  </div>
  <div class="h-[1.5px] bg-slate-950 w-1/4 mr-auto mb-4 mt-2"></div>
  <div class="flex flex-wrap items-center gap-2 mb-4 text-xs sm:text-sm">
      {#each reviewItem.features as feature}
          <div
              class="p-1 py-0.5 rounded-md border border-solid border-indigo-400 bg-indigo-50 text-indigo-400"
          >
              <p>{feature}</p>
          </div>
      {/each}
  </div>
  <p>{reviewItem.review}</p>
</div>