<script>
  import Logo from './Logo.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
  import { page } from '$app/stores';
</script>

<header>
  {#if $page.url.pathname !== '/'}
    <a href="/"><Logo fontSize={2}/></a>
  {/if}
  <nav style="">
    <a href="/about">about us</a>
    <span class="icon"><FaGithub /></span>
  </nav>
</header>

<style>
  header {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding: 1rem 2rem;
    color: var(--white);
  }
  a {
    font-size: 2rem;
    font-weight: 400;
    font-family: 'Karla';
    text-decoration: none;
  }
	.icon {
		display: inline-block;
		width: 32px;
		height: 32px;
	}
  nav {
    width: 100%;
    display: flex;
    justify-content:flex-end;
    gap: 1rem;
  }
  nav > a {
    font-size: 1rem;
		font-weight: 400;
		color: var(--white);
		padding: 0.25rem 0.5rem;
		display: flex;
		align-items: center;
		border-radius: 4px;
		cursor: pointer;
		text-decoration: none;
		border: 1px solid var(--white);
	}
</style>