<script lang="ts">
  import { onMount } from "svelte"
  import lottie from 'lottie-web'
	import Step from "./Step.svelte";

  // import animationData from '../../static/assets/compute.json'

  let animationContainer: HTMLElement
  let steps = [
    {name: 'CloudThings', icon: 'fa-brands fa-cloudversify'}, 
    {name: 'DevSecOps', icon: 'fa-solid fa-microchip'}, 
    {name: 'Linux OS', icon: 'fa-solid fa-terminal'}, 
    ]

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

  <section id="projects" class="py-20 lg:py32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
        <h6 class="text-large sm:text-xl md:text-2xl">
          A few creations
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
          Curious to <span class="poppins text-violent-400">see</span> my work?
        </h3>
    </div>
    <a href="https://github.com/JacksVDF" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200">
      <i class="fa-regular fa-circle-play"></i>
      <p>Watch my Github!</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>Cloud things are just that, things developed for Cloud Purposes</p>
        <strong class="text-violet-400">Docker, Kubernetes & AWS/Azure</strong> All these tech is for Cloud.
      </Step>
      <Step step={steps[1]}>
        <p>DevSecOps are projects with a clear objective, practice these behaviors</p>
        <strong class="text-violet-400">Jira, Jenkins, JFrog, Prometheus & Others</strong> All these tech is for DevSecOps.
      </Step>
      <Step step={steps[2]}>
        <p>These Linux Open Source projects are meant to be used for the community and my Research Group GEHIRN</p>
        <strong class="text-violet-400">LinuxOS, Bash, Terminal & OS Software</strong> All these tech is for OpenSource projects.
      </Step>
    </div>
  </section>

</main>