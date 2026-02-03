<script lang="ts">
	import Header from './Header.svelte';
	import './layout.css';

	let { children } = $props();
</script>

 <div class="navbar bg-base-100 shadow-sm">
  <div class="navbar-start">
    <div class="dropdown">
      <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"> <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h8m-8 6h16" /> </svg>
      </div>
      <ul
        tabindex="-1"
        class="menu menu-sm dropdown-content bg-base-100   rounded-box z-1 mt-3 w-52 p-2 shadow">
        <li><a>Item 1</a></li>
        <li>
          <a>Parent</a>
          <ul class="p-2">
            <li><a>Submenu 1</a></li>
            <li><a>Submenu 2</a></li>
          </ul>
        </li>
        <li><a>Item 3</a></li>
      </ul>
    </div>
    <a href="/portfolio" class="btn btn-ghost text-xl">Home</a>
  </div>
  <div class="navbar-end hidden lg:flex flex justify-items-end">
    <ul class="menu menu-horizontal">
      <li><a href="/portfolio/about me" >About Me</a></li>
      <li>
        <details>
          <summary>Projects</summary>
          <ul class="p-2 bg-base-100 w-40 z-1">
            <li><a href="/">html/Pokedex</a></li>
            <li><a href="/portfolio/about me/communication designs">The Southpark Mystery</a></li>
          </ul>
        </details>
      </li>
      <li><a href="/portfolio/others">Contact</a></li>
    </ul>
  </div>
 
</div>



<div class="app">
	<main>{@render children()}</main>
</div>

