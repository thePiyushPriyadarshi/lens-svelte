<script>
    export let cardData
</script>

<div
class={`relative flex flex-col justify-between w-[336px] h-[435px] bg-white dark:hover:bg-black  hover:bg-transparent z-10  border-transparent rounded-[30px] dark:bg-[#1b1c1e] hover:border-[#FF9F31] group border pt-8 p-6`}
>
<!-- {/* <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-b from-[#01c99b] via-teal-100 to-transparent blur-2xl opacity-35 z-0"></div> */} -->
<p class="text-3xl font-semibold dark:text-white text-black">{cardData.title}</p>
<div class="relative image-container-4 group-hover:opacity-100 w-[125px] h-[160px] mx-auto">
  <img fill src={cardData.img} alt="img" />
</div>
<div class="dark:text-[#8A8A8A] text-black">{cardData?.desc}</div>
</div>