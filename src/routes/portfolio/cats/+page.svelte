<script lang="ts">
	import { goto } from "$app/navigation";

</script>
<div>
    <div class="hero bg-orange-100 min-h-screen">
  <div class="hero-content flex-col lg:flex-row">
    <img  class="w-150 max-h-100" src="https://cataas.com/cat"/>
    <div>
      <h1 class="text-5xl font-bold text-red-300">Cats against raging</h1> <br>
      <button class="btn bg-red-300 text-rose-500" onclick={() => window.location.reload() }>les goo</button>
      
      <button class="btn bg-red-300 text-rose-500" onclick={() =>goto('/portfolio/cats/catgif') }>surprise</button>
      
    </div>
  </div>
</div>

</div> 



