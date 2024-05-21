<script>
  import MobileNavar from "./MobileNavar.svelte";
  import { onMount } from 'svelte';
  const navbarOptions = [
    {
      label: "Home",
      path: "/",
    },
    {
      label: "Company",
      path: "#company",
    },
    {
      label: "Blogs",
      path: "#blogs",
    },
  ];
  let isLogin = false;

  onMount(() => {
    const token = localStorage.getItem('token');
    if (token) {
      isLogin = true;
    }
  }); 

  function logout(){
    localStorage.removeItem('token');
    isLogin = false;
  }
</script>

<nav
  class="bg-white fixed top-0 dark:bg-transparent z-50 w-full backdrop-blur-3xl text-black dark:text-white py-3"
>
  <div class="w-11/12 lg:w-10/12 mx-auto flex justify-between items-center">
    <div class="dark:hidden block">
      <img
        width={80}
        height={80}
        src={"https://lenscorp.ai/_next/image?url=%2F_next%2Fstatic%2Fmedia%2Fnav_logo.e5fb945a.png&w=96&q=75"}
        alt="logo"
      />
    </div>
    <div class="dark:block hidden">
      <img
        width={80}
        height={80}
        src={"https://lenscorp.ai/_next/image?url=%2F_next%2Fstatic%2Fmedia%2FnewLogo.9985891c.png&w=96&q=75"}
        alt="logo"
      />
    </div>
    <div class="hidden lg:block">
      <div class="flex gap-6 items-center justify-center">
        <a href="https://makemyweb.ai/en" target="_blank">MakeMyWeb.</a>
        <!-- {
              navbarOptions.map((option,i)=>(
                  <Link key={i} class={`${route(option.path) ? "bg-gradient-to-r text-transparent from-[#0796FF] to-[#91F6FF]" : ""}  font-semibold bg-clip-text`} href={option.path}>{option.label}</Link>
              ))
          } -->
        {#each navbarOptions as option}
          <a
            class={`${option.path == "/" ? "bg-gradient-to-r text-transparent from-[#0796FF] to-[#91F6FF]" : ""} font-semibold bg-clip-text`}
            href={option.path}>{option.label}</a
          >
        {/each}
        {#if isLogin == false}
          <div>
            <a
              class="bg-white border px-4 py-2 rounded-lg text-black"
              href="/register">Register</a
            >
            <a
              class="border rounded-lg hover:bg-gray-800 px-4 py-2"
              href="/login">Login</a
            >
          </div>
          {:else if isLogin == true}
           <button on:click={logout} class="border px-4 py-2 rounded-lg">Log Out</button>
        {/if}
 
      </div>
    </div>
    <div class="block lg:hidden">
      <MobileNavar />
    </div>
  </div>
</nav>
