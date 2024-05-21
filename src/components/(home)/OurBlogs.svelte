<script>

  import BlogCard from "./(blog)/BlogCard.svelte";

</script>
<div id="blogs" class="flex dark:text-white mb-20 text-black flex-col items-center justify-center">
    <div class="w-fit mt-20">
      <h2 class="text-2xl font-semibold uppercase my-1">Our Blogs</h2>
      <div class="bg-gradient-to-r from-[#0796FF] to-[#91F6FF] rounded-lg mx-auto w-8/12 h-[4px]"></div>
    </div>
    <div class="lg:text-7xl max-w-[1080px] text-center my-10 md:text-5xl text-3xl">
      <p>Inhouse Mindscape</p>
    </div>
    <BlogCard/>
     <!-- <ArrowRight class="hidden group-hover/button:block transition-all duration-200 w-4 h-4 ml-2"/>  -->
    <button   class="w-fit text-xl px-6 py-3 my-10 rounded-xl group/button border border-black dark:text-white text-black dark:border-white bg-transparent hover:bg-black dark:hover:bg-white dark:hover:text-black hover:text-white">Explore More 
    </button>


  </div>