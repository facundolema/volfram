<script lang="ts">
	import ProjectCard from '$lib/ProjectCard.svelte';
	import Logo from '$lib/Logo.svelte';
</script>

<main>
	<Logo fontSize={6} />
	<div class="card-container">
		<ProjectCard title="Seagull" logo="seagull.png">
			Your complete guide to global exploration! Discover countries and places with concise
			insights. From landscapes to culture, get quick access to essential details. Plan your next
			adventure or find inspiration - Seagull, where information meets adventure!
		</ProjectCard>
		<ProjectCard title="Appleseed" logo="seagull.png">
			Your complete guide to global exploration! Discover countries and places with concise
			insights. From landscapes to culture, get quick access to essential details. Plan your next
			adventure or find inspiration - Seagull, where information meets adventure!
		</ProjectCard>
		<ProjectCard title="GeoHuemul" logo="seagull.png">
			Your complete guide to global exploration! Discover countries and places with concise
			insights. From landscapes to culture, get quick access to essential details. Plan your next
			adventure or find inspiration - Seagull, where information meets adventure!
		</ProjectCard>
		<ProjectCard title="Quaver" logo="seagull.png">
			A P2P-powered mobile music player with local, personalized analytics akin to Spotify Wrapped
			to explore your music habits. Quaver is an open-source project built on React Native. Enjoy
			customization, interoperability, and embrace a decentralized, community-driven approach to
			music consumption.
		</ProjectCard>
	</div>
</main>

<style>
	.card-container {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 2rem;
		justify-content: center;
		align-items: center;
	}
	@media (max-width: 50rem) {
		.card-container {
			grid-template-columns: 1fr;
		}
	}
</style>
