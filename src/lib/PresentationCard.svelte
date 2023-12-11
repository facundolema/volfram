<script lang="ts">
	import Dropdown from './Dropdown.svelte';
	export let title: string;
	export let image: string;
	export let tags: string[];
	export let cv: string;
	export let portfolios: { name: string; link: string }[];
	export let more: string;
</script>

<div class="card">
	<div class="picture">
		<img src={image} alt={title} />
	</div>
  <h2>{title}</h2>
	<div class="tags">
		{#each tags as tag}
			<span class="tag">{tag}</span>
		{/each}
	</div>
	<p>
		<slot />
	</p>
	<div class="links">
		<Dropdown portfolios={portfolios} />
		<a href={cv} class="actions">CV &downarrow;</a>
		<a href={more} class="actions">+</a>
	</div>
</div>

<style>
	.actions {
		font-weight: 400;
		color: var(--primary);
		padding: 0.25rem 0.5rem;
		border-radius: 4px;
		cursor: pointer;
		text-decoration: none;
		display: flex;
		align-items: center;
		border: 1px solid var(--primary);
		position: relative;
	}
	.card {
		border: 1px solid var(--primary);
		width: 16rem;
		display: flex;
		padding: 1rem;
		flex-direction: column;
		align-items: flex-start;
		justify-content: space-between;
		border-radius: 4px;
		transition: all 0.5s ease;
		gap: 1rem;
	}
	.picture {
		border: 1px solid var(--primary);
		width: 100%;
		aspect-ratio: 1;
		border-radius: 4px;
		overflow: hidden;
	}
	.links {
		display: flex;
		flex-direction: row;
		width: 100%;
		gap: 0.5rem;
		justify-content: flex-end;
	}
	h2 {
		font-size: 2rem;
		font-weight: 600;
		font-family: 'Karla';
		margin: 0;
	}
	p {
		margin: 0;
	}
	.tag {
		font-size: 0.75rem;
		padding: 0.125rem 0.5rem;
		background-color: var(--primary);
		color: var(--black);
		border-radius: 4px;
		margin: 0;
	}
	.tags {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		gap: 0.5rem;
	}
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

</style>
