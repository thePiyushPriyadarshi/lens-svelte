<script>
 import {goto} from "$app/navigation"
  let email = "";
  let password = "";
  let name = ""
  let error = ""
  let isLoading = false;
  function handleSubmit(event) {
    event.preventDefault();
     isLoading = true; 
	fetch("https://golang-production-ebec.up.railway.app/register",{
		method: "POST",
		body: JSON.stringify({
			email,
      name,
			password
		}),
		headers : {
			"Content-Type": "application/json; charset=UTF-8",
		}
	}).then((response) => response.json())
	.then((json)=> {alert(json.message)
		isLoading=false
		if(json.status) goto("/login")
	})
	.catch((error) => {
    console.error('Error:', error);
});
 
    email = "";
    password = "";
    name = "";
  }
</script>

<div class="min-h-screen mt-32">
  <div
    class="max-w-[480px] hover:border-[#34D4AE] border-2 shadow-[#34D4AE] hover:shadow-2xl bg-zinc-900 hover:bg-transparent flex flex-col items-center gap-10 w-11/12 mx-auto border-gray-300 rounded-lg py-14"
  >
    <h3 class="flex flex-col text-xl">
      Register to
      <span
        class="bg-gradient-to-r font-semibold from-[#0796FF] to-[#91F6FF] bg-clip-text text-transparent"
        >LENS CORPORATION</span
      >
    </h3>
    <form class="flex flex-col items-center gap-6" on:submit={handleSubmit}>
      
      <label class="flex flex-col gap-1">
        <p class="text-left">Full Name <sup class="text-rose-500">*</sup></p>
        <input
		required
          class="bg-gray-800 w-[320px] text-white rounded-lg py-2 px-4"
          type="text"
          placeholder="Enter your name"
          bind:value={name}
        />
      </label>
      <label class="flex flex-col gap-1">
        <p class="text-left">Email <sup class="text-rose-500">*</sup></p>
        <input
		required
          class="bg-gray-800 w-[320px] text-white rounded-lg py-2 px-4"
          type="email"
          placeholder="Enter your email"
          bind:value={email}
        />
      </label>
      <label class="flex flex-col gap-1">
        <p class="text-left">Password <sup class="text-rose-500">*</sup></p>
        <input
		required
          class="bg-gray-800 w-[320px] text-white rounded-lg py-2 px-4"
          type="password"
          placeholder="Enter your password"
          bind:value={password}
        />
      </label>
	  <p class="text-left text-rose-500">{error}</p>
      <button
	  disabled={isLoading}
	  type="submit"
        class="border-white disabled:bg-gray-400 hover:bg-white hover:text-black transition-all duration-200 border px-6 py-2 w-[320px] rounded-lg"
        >Login</button
      >
    </form>
  </div>
</div>
