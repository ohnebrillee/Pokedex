<script lang="ts">
	import { goto } from "$app/navigation";

</script>
<div class="hero bg-orange-100 min-h-screen">
  <div class="hero-content flex-col lg:flex-row">
    <img  class="w-150 max-h-150" src="https://cataas.com/cat/gif"/>
    <div>
      <h1 class="text-5xl font-bold text-red-300">rather want a gif?</h1> <br>
      <button class="btn bg-red-300 text-rose-500" onclick={() => window.location.reload() }>les goo</button>
      <button class="btn bg-red-300 text-rose-500" onclick={() =>goto('/portfolio/cats') }>go back</button>
    </div>
  </div>
</div>
