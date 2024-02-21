<script lang="ts">
  import { onMount } from "svelte"
  import lottie from 'lottie-web'

  // import animationData from '../../static/assets/compute.json'

  let animationContainer: HTMLElement

  onMount(()=>{
    lottie.loadAnimation({
      container: animationContainer,
      // #TODO Need revision for Bad Request Management, try to use compute.json file in Assets instead of a link
      path: 'https://lottie.host/420fdca4-68a7-4169-9c72-27f9b0592034/T3D7LZoCka.json',
      loop: true,
      autoplay: true,
    })
  })
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
      <h2 class="font-semibold text-4xl sm:text5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Julian</span> Cardona <br/> Software <span class="poppins text-violet-400">Craftsman</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400"> expertise</span> includes Cloud (OpenShift, IBM Cloud) and DevSecOps
      </p>
      <a href="https://www.linkedin.com/in/jacksvdf/" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-violet-800 text-salte-950 cursor-pointer">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
        <h4 class="relative z-9">Get in Touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
        <div bind:this={animationContainer} style="width: 85%; height: 85%">
    </div>
  </section>
</main>