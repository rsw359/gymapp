<script>
  import "../app.css";
  import Footer from "../components/Footer.svelte"
  import Header from "../components/Header.svelte"
  import {openModal} from "../store"
  import Cta from "../components/CTA.svelte";
  let y

  $: outerHeight = 0 

  function reroute(href) {
    $openModal = false;
    location.href = href;
  } 
 
</script>
{#if $openModal}
  <div class="fixed top-0 left-0 z-50 flex flex-col w-screen h-screen gap-8 p-5 px-8 bg-white border-b md:hidden">

     <div class="flex items-center justify-between gap-4 pb-2 border-b">
      <h1 class="font-semibold">Gym<span class="text-indigo-400">Helper</span></h1> 
      <button class="border-none outline-none" on:click={()=> $openModal = false}>
        <i class="text-2xl fa-solid fa-xmark "></i>
      </button>
     </div>
     <div class="flex flex-col flex-1 gap-4">
      <button on:click={()=>reroute("#product")} class="p-2 text-left duration-200 border-none outline-none cursor-pointer group">
        <p class="duration-200 group-hover:pl-2">Product</p>
      </button>
    
     
      <button on:click={()=>reroute("#reviews")} class="p-2 text-left duration-200 border-none outline-none cursor-pointer group">
        <p class="duration-200 group-hover:pl-2">Reviews</p >
      </button>
    
     
      <button on:click={()=>reroute("#faq")} class="p-2 text-left duration-200 border-none outline-none cursor-pointer group">
        <p class="duration-200 group-hover:pl-2">FAQs</p>
      </button>
    </div>
    
    <Cta/>
  </div>
{/if}

{#if y > outerHeight}
  <div class="fixed top-0 left-0 z-20 flex flex-col w-full px-4 bg-white fade-in">
    <Header/>
  </div>
{/if}
<slot />
<Footer/>
<svelte:window bind:scrollY={y} bind:outerHeight/>
