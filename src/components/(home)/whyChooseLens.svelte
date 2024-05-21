<script>
  import ChooseCard from "./(whychoose)/ChooseCard.svelte";

  const list = [
    "State-of-the-art solutions",
    "Lifetime support & upgrades",
    "Fast & Efficient",
    "Plug-and-Play",
    "No extra computation fee",
    "24x7 Progress Monitoring",
    "No licensing fee",
    "Incremental Updates",
  ];
</script>

<div class="flex flex-col my-24 items-center justify-center">
  <div
    class="flex gap-2 dark:text-white text-black font-semibold text-2xl uppercase"
  >
    {" "}
    Why
    <div class="w-fit">
      <h2 class="">Choose</h2>
      <div
        class="bg-gradient-to-r mt-1 from-[#0796FF] to-[#91F6FF] rounded-lg mx-auto w-8/12 h-[5px]"
      ></div>
    </div>
    Lens
  </div>
  <div
    class="lg:text-7xl dark:text-white text-black max-w-[1080px] text-center mt-16 mb-10 md:text-5xl text-3xl"
  >
    <p>AI-driven solutions backed by science</p>
  </div>
  <div
    class="lg:text-2xl max-w-[980px] dark:text-[#8A8A8A] text-black text-center text-xl"
  >
    <p>
      Every piece of AI technology shipped from LENS is thoroughly benchmarked
      via rigorous evaluations. With a global network of experts and
      academicians, we guarantee the most accurate and robust solutions in the
      market.
    </p>
  </div>
  <div class="mt-10">
    <ul
      class="grid lg:grid-cols-2 dark:text-white text-black gap-4 grid-cols-1"
    >
      {#each list as item}
      <li class="flex gap-2 items-center">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          x="0px"
          y="0px"
          width="20"
          height="20"
          viewBox="0,0,256,256"
        >
          <g
            fill="#ffffff"
            fill-rule="nonzero"
            stroke="none"
            stroke-width="2"
            stroke-linecap="butt"
            stroke-linejoin="miter"
            stroke-miterlimit="10"
            stroke-dasharray=""
            stroke-dashoffset="0"
            font-family="none"
            font-weight="none"
            font-size="none"
            text-anchor="none"
            style="mix-blend-mode: normal"
            ><g transform="scale(8.53333,8.53333)"
              ><path
                d="M26.98047,5.99023c-0.2598,0.00774 -0.50638,0.11632 -0.6875,0.30273l-15.29297,15.29297l-6.29297,-6.29297c-0.25082,-0.26124 -0.62327,-0.36647 -0.97371,-0.27511c-0.35044,0.09136 -0.62411,0.36503 -0.71547,0.71547c-0.09136,0.35044 0.01388,0.72289 0.27511,0.97371l7,7c0.39053,0.39037 1.02353,0.39037 1.41406,0l16,-16c0.29576,-0.28749 0.38469,-0.72707 0.22393,-1.10691c-0.16075,-0.37985 -0.53821,-0.62204 -0.9505,-0.60988z"
              ></path></g
            ></g
          >
        </svg>
        <p class="flex gap-2"><span class="font-medium">{item}</span></p>
      </li>
      {/each}
    </ul>
  </div>
  <ChooseCard />
</div>
