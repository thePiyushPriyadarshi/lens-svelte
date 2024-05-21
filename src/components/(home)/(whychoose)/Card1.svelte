<script>
    export let cardData
</script>

<div
class={`relative flex flex-col justify-between w-[336px] h-[435px] z-10 border border-transparent rounded-[30px] hover:bg-transparent bg-white dark:hover:bg-black dark:bg-[#1b1c1e] hover:border-[#34D4AE] group pt-8 p-6`}
>
<!-- {/* <div class="absolute -top-10 -left-10 w-full h-[300px] bg-gradient-to-b from-[#01c99b] via-teal-100 to-transparent blur-2xl opacity-35 -z-10"></div> */} -->
<p class="text-3xl font-semibold dark:text-white text-black">{cardData.title}</p>
<div class="relative image-container-1 group-hover:opacity-100 w-[251px] h-[91px] mx-auto">
  <img fill src={cardData.img} alt="img" />
</div>
<div class="dark:text-[#8A8A8A] text-black">{cardData?.desc}</div>
</div>