<script>
  let isOpen = false;
  import { onMount } from "svelte";

  function toggleMenu() {
    isOpen = !isOpen;
  }
  const navbarOptions = [
    {
      label: "Home",
      path: "/",
    },
    {
      label: "Company",
      path: "/",
    },
    {
      label: "Blogs",
      path: "/",
    },
  ];
  let isLogin = false;

  onMount(() => {
    const token = localStorage.getItem("token");
    if (token) {
      isLogin = true;
    }
  });

  function logout() {
    localStorage.removeItem("token");
    isLogin = false;
  }
</script>

<div class="navbar">
  <div class="menu-icon" on:click={toggleMenu}>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="24"
      height="24"
      viewBox="0 0 24 24"
      ><path d="M0 0h24v24H0z" fill="none" /><path
        d="M4 18h16c.55 0 1-.45 1-1s-.45-1-1-1H4c-.55 0-1 .45-1 1s.45 1 1 1zm0-5h16c.55 0 1-.45 1-1s-.45-1-1-1H4c-.55 0-1 .45-1 1s.45 1 1 1zM3 7c0 .55.45 1 1 1h16c.55 0 1-.45 1-1s-.45-1-1-1H4c-.55 0-1 .45-1 1z"
      /></svg
    >
  </div>
  <div class="menu {isOpen ? 'active' : ''}">
    {#each navbarOptions as option}
      <a
        class={`${option.path == "/" ? "bg-gradient-to-r text-transparent from-[#0796FF] to-[#91F6FF]" : ""} font-semibold bg-clip-text`}
        href={option.path}>{option.label}</a
      >
    {/each}
    {#if isLogin == false}
      <div class="flex flex-col gap-2 pb-4">
        <a
          class=" border px-5 py-1 rounded-lg text-black"
          href="/register">Register</a
        >
        <a class="border rounded-lg hover:bg-gray-800 px-5 py-1" href="/login"
          >Login</a
        >
      </div>
    {:else if isLogin == true}
      <button on:click={logout} class="border px-4 py-1 mb-4 rounded-lg"
        >Log Out</button
      >
    {/if}
  </div>
</div>

<style>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    color: white;
  }

  .menu-icon {
    background-color: white;
    border-radius: 100%;
    padding: 4px;
    display: none;
    cursor: pointer;
  }

  .menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  @media (max-width: 1024px) {
    .menu {
      display: none;
      flex-direction: column;
      position: absolute;
      top: 6rem;
      right: 0;
      width: 50%;
      background-color: black;
    }

    .menu.active {
      display: flex;
    }

    .menu a {
      padding: 1rem;
      color: white;
      text-decoration: none;
    }

    .menu a:hover {
      background-color: #555;
    }

    .menu-icon {
      display: block;
    }
  }
</style>
