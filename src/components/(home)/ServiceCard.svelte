<script>
  import Card1 from "./(sevice)/Card1.svelte";
  import Card2 from "./(sevice)/Card2.svelte";
  import Card3 from "./(sevice)/Card3.svelte";
  import Card4 from "./(sevice)/Card4.svelte";

  export let data;
</script>


<div class="grid grid-cols-1 lg:grid-cols-2 gap-6 my-10 max-w-[1080px]">
  <div class="relative">
    <div
      class="absolute w-[300px] -top-12 z-0 -left-12 aspect-square dark:bg-transparent bg-[#34d4afa9] blur-[150px] "
    ></div>
    <Card1 cardData={data[0]} />
  </div>
  <div class="relative">
    <div
      class="absolute w-[300px] -top-12 z-0 -right-12 aspect-square dark:bg-transparent bg-[#69bfe7a7] blur-[150px] "
    ></div>
    <Card2 cardData={data[1]} />
  </div>
  <div class="relative">
    <div
      class="absolute w-[300px] -bottom-12 z-0 -left-12 aspect-square dark:bg-transparent bg-[#ff5f5f79] blur-[150px] "
    ></div>
    <Card3 cardData={data[2]} />
  </div>
  <div class="relative">
    <div
      class="absolute w-[300px] -bottom-12 z-0 -right-12 aspect-square dark:bg-transparent bg-[#ff9f3177] blur-[150px] "
    ></div>
    <Card4 cardData={data[3]} />
  </div>
</div>




