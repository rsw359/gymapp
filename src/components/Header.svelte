 <script>
  import { openModal } from "../store";
    

 </script>
 
 <header class="relative z-20 flex flex-col">
    <div class="max-v-[1400] mx-auto w-full flex items-center  justify-between p-4 py-6">
       <a href="/">
        <h1 class="font-semibold">Gym<span class="text-indigo-400">Helper</span></h1>
       </a>
       <button class="grid md:hidden place-items-center" on:click={() => ($openModal = true)}>
         <i class="fa-solid fa-bars"></i>
       </button>
       <nav class="items-center hidden gap-4 md:flex lg:gap-6">
         <a class="duration-200 cursor-pointer hover:text-indigo-500" href="#product">Product</a>
         <a class="duration-200 cursor-pointer hover:text-indigo-500" href="#reviews">Reviews</a>
         <a class="duration-200 cursor-pointer hover:text-indigo-500" href="#faq">FAQ</a>
         <button class="specialBtn">
          <p>Start Free Today</p>
         </button>  
       </nav>
    </div> 

 </header> 