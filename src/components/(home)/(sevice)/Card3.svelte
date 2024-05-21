<script>
    export let cardData;
  </script>

<div
class={`relative z-10 border-transparent rounded-xl dark:bg-[#1b1c1e] dark:hover:bg-black bg-white hover:bg-transparent hover:border-[#FF605F] group border p-10`}
>
<!-- {/* <div class="absolute bottom-0 right-0 w-full h-full dark:hidden group-hover:bg-gradient-to-tr from-[#FF605F] to-[#ecfffb] blur-2xl opacity-0 z-0"></div> */} -->

<div class="flex items-center">
  <p class="text-8xl flex text-muted-foreground/25 font-semibold">
    <span>0</span>
    <span class={`group-hover:text-[#FF605F]`}>
      {cardData?.index}
    </span>
  </p>
  <p
    class={`-ml-14 mt-10 max-w-[250px] group-hover:translate-x-10 transition-all duration-300 text-4xl text-[#FF605F] group-hover:text-[#8A8A8A] font-semibold`}
  >
    {cardData?.title}
  </p>
</div>
<div class="mt-16 dark:text-[#8A8A8A] text-black text-xl leading-8 font-semibold">
  {cardData?.desc}
</div>
</div>