<script>
    
    let darkMode = false;

    function handleSwitchDarkMode() {
        darkMode = !darkMode;

        darkMode
            ? document.documentElement.classList.add('dark')
            : document.documentElement.classList.remove('dark');
    }
</script>


{#if darkMode = false}
<button on:click={handleSwitchDarkMode}>
    <!-- <Moon />{" "} --> Dark
  </button>
{:else if darkMode = true}
<button onClick={() => {}}>
    <!-- <Sun className="text-yellow-500" />{" "} -->
light 
</button>
{/if}