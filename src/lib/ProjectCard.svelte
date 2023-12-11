<script lang="ts">
  export let title: string;
  export let logo: string;
</script>

<div class="card">
  <div class="title">
    <div class="logo" />
    <h2>{title}</h2>
    <span class="tag">blog</span>
  </div>
  <p>
    <slot />
  </p>
  <div class="links">
    <a href="/seagull" class="secondary-link">Source &#x2197;</a>
    <a href="/seagull" class="primary-link">Learn more</a>
  </div>
</div>

<style>
  	a {
		font-weight: 400;
		color: var(--primary);
		padding: 0.25rem 0.5rem;
		border-radius: 4px;
		cursor: pointer;
    text-decoration: none;
    &.primary-link {
      border: 1px solid var(--primary);
    }
	}
  .card {
		border: 1px solid var(--primary);
		width: 20rem;
		aspect-ratio: 4/3;
		display: flex;
		padding: 1rem;
		flex-direction: column;
		align-items: flex-start;
		justify-content: space-between;
    border-radius: 4px;
	}
	.logo {
		border: 1px solid var(--primary);
		width: 2rem;
		height: 2rem;
    border-radius: 4px;
	}
	.title {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
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
		margin-left: 1rem;
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
    font-weight: 600;
    margin: 0;
    font-family: 'Space Mono';
    margin-left: 0.5rem;
  }
</style>