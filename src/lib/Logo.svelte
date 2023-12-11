<script lang="ts">
	export let fontSize: number;
</script>

<div class="logo">
	<span id="volfram" style="font-size: {fontSize}rem; line-height: {fontSize}rem">Volfram</span>
	<span id="studio" style="font-size: {fontSize/2}rem; line-height: {fontSize/2}rem">Studio</span>
</div>

<style>
  #volfram {
    font-size: 2rem;
    font-weight: 600;
    line-height: 2rem;
    margin: 0;
  }
  #studio {
    font-size: 1rem;
    line-height: 1rem;
    font-weight: 400;
    margin: 0;
  }
  .logo {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    font-family: 'Karla';
    color: var(--white);
  }
</style>