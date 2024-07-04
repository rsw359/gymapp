<script>
  import SectionWrapper from "./SectionWrapper.svelte";
  let faqs =
    [
    {
        "question": "What is GymHelper?",
        "answer": "GymHelper is a fun fitness app designed to make your workouts enjoyable by incorporating interactive games and challenges."
    },
    {
        "question": "Can I track my progress with GymHelper?",
        "answer": "Yes, GymHelper allows you to track your workout progress, set fitness goals, and monitor your achievements over time."
    },
    {
        "question": "Does GymHelper offer personalized workout plans?",
        "answer": "Yes, GymHelper provides personalized workout plans based on your fitness level, goals, and preferences."
    },
    {
        "question": "Is GymHelper suitable for beginners?",
        "answer": "Absolutely! GymHelper offers a variety of workouts and challenges suitable for all fitness levels, including beginners."
    },
    {
        "question": "Can I use GymHelper without an internet connection?",
        "answer": "Yes, you can access your saved workout plans and track your progress offline. However, some features may require an internet connection."
    },
    {
        "question": "Are there any subscription fees for using GymHelper?",
        "answer": "GymHelper offers both free and premium subscription options. The premium subscription provides additional features and personalized plans."
    },
    {
        "question": "How can I contact GymHelper support?",
        "answer": "You can contact GymHelper support by emailing support@gymhelper.com."
    },
    
]

</script>

<SectionWrapper id='faq'>
  <div class="flex flex-col items-center justify-center flex-1 gap-10 py-20 sm:gap-14 md:gap-24 ">
   <div class="flex flex-col gap-2">
       <p class="text-base text-center opacity-60 sm:text-lg md:text-xl">Any questions or qalms?</p>
       <h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">Frequently Asked
         <span class="text-indigo-400">Questions</span></h3>
   </div>
   <div class="flex flex-col w-full gap-4 sm:gap-8 md:gap-6">
    {#each faqs as faq}
    <div class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6">
    <h4 class="pt-2 text-lg text-indigo-400 sm:text-xl md:text-2xl">
      {faq.question}
    </h4>
      <p class="pl-2">{faq.answer}</p>
    </div>
   {/each}
   </div>
  </div>
</SectionWrapper>
  