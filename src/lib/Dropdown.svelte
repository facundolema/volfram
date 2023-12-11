<script lang="ts">
	import MdKeyboardArrowDown from 'svelte-icons/md/MdKeyboardArrowDown.svelte';

	export let portfolios: { name: string; link: string }[] = [];
</script>

<div class="dropdown-btn">
	Portfolios <span class="icon"><MdKeyboardArrowDown /></span>
	<div class="dropdown-content">
		{#each portfolios as portfolio}
			<a href={portfolio.link} class="dropdown-entry">
				<span>{portfolio.name}</span>
				<span class="dropdown-entry-icon">→</span>
			</a>
		{/each}
	</div>
</div>

<style>
	.dropdown-btn {
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
		&:hover .dropdown-content {
			opacity: 1;
			transition: opacity 0s;
		}
	}
	.dropdown-content {
		position: absolute;
		top: calc(100% + 0.5rem);
		width: min-content;
		left: 0;
		border: 1px solid var(--primary);
		border-radius: 4px;
		opacity: 0;
		display: flex;
		flex-direction: column;
		gap: 0.25rem;
		background-color: var(--background);
		transition: opacity 0s 0.25s;
	}
	.dropdown-entry {
		color: var(--primary);
		text-decoration: none;
		padding: 0.25rem 0.5rem;
		display: flex;
		gap: 1rem;
		justify-content: space-between;
		&:hover {
			background-color: var(--primary-transparent);
			& .dropdown-entry-icon {
				opacity: 1;
			}
		}
	}
	.icon {
		margin-left: 0.25rem;
		height: 1rem;
		width: 1rem;
		display: inline-block;
	}
	.dropdown-entry-icon {
		opacity: 0;
	}
</style>
