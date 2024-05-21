<script>
  import Card1 from "./Card1.svelte";
  import Card2 from "./Card2.svelte";
  import Card3 from "./Card3.svelte";
  import Card4 from "./Card4.svelte";
  export const chooseLens = [
    {
      title: "Exclusive Rights",
      img: "https://lenscorp.ai/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fgreen.e71c8735.png&w=256&q=75",
      desc: "Our mission is to make an impact in empowering human society with AI. Hence, all Intellectual Property Rights belongs to you.",
    },
    {
      title: "Research Driven",
      img: "https://lenscorp.ai/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fblue.f22859fe.png&w=256&q=75",
      desc: "We regularly benchmark our solutions via comparing industry-vide evaluations so our partners only get the best that AI can offer.",
    },
    {
      title: "Plug-and-Play",
      img: "https://lenscorp.ai/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fred.a7efdb29.png&w=128&q=75",
      desc: "We provide AI-driven solutions into businesses where they can bring tangible value. Each solution is customized as per your needs and deployed on any computing device of your choice.",
    },
    {
      title: "Lifetime Support",
      img: "https://lenscorp.ai/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fyellow.d937d179.png&w=256&q=75",
      desc: "Should you face any issues, we are always at your service. We provide lifetime technical support & upgrade options.",
    },
  ];
</script>

<div class="my-20 flex flex-wrap justify-center gap-5 w-[95%] mx-auto">
  <div class="relative h-full">
    <div
      class="absolute w-[300px] -top-12 z-0 -left-12 aspect-square dark:bg-transparent bg-[#34d4afa9] blur-[150px]"
    ></div>
    <Card1 cardData={chooseLens[0]} />
  </div>
  <div class="relative">
    <div
      class="absolute w-[300px] -top-12 z-0 -left-12 aspect-square dark:bg-transparent bg-[#69bfe7a7] blur-[150px]"
    ></div>
    <Card2 cardData={chooseLens[1]} />
  </div>
  <div class="relative">
    <div
      class="absolute w-[300px] -top-12 z-0 -left-12 aspect-square dark:bg-transparent bg-[#69bfe7a7] blur-[150px]"
    ></div>
    <Card3 cardData={chooseLens[2]} />
  </div>
  <div class="relative">
    <div
      class="absolute w-[300px] -top-12 z-0 -left-12 aspect-square dark:bg-transparent bg-[#ff9f3177] blur-[150px]"
    ></div>
    <Card4 cardData={chooseLens[3]} />
  </div>
</div>
