<script>
  import SectionWrapper from "./SectionWrapper.svelte"
  import Header from "./Header.svelte"
  import Cta from "./CTA.svelte";
	import Stars from "./Stars.svelte";
</script>
<SectionWrapper>
    <Header/>
    <div class="flex flex-col items-center justify-center flex-1 gap-10 pb-10 md:pb-14">
      <h2 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center">
        <span class="text-indigo-400">Working out</span>
        <span class="line-through text-slate-600">is hard</span><br/>
        just got <span class="italic text-indigo-400">EASIER</span>
      </h2>
      <p class="text-xl sm:text-2-xl md:text-3xl text-center max-w-[1000px] mx-auto w-full">
        Less thinking, more doing. We're the trainer in your pocket with <span class="italic text-indigo-400">Personalized workouts, detailed explanations, analytics,</span> and much, much more...
      </p>  
      <Cta/>
      <Stars/>
    </div>
</SectionWrapper>