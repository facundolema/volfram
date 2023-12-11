<script>
	import PresentationCard from '$lib/PresentationCard.svelte';
</script>

<main>
	<h1>About us</h1>
	<p>
		We are a group of developers who are passionate about music and technology. We believe that
		music is a universal language that can bring people together. We also believe that technology
		can be used to empower people and help them achieve their goals.
	</p>
	<h1>The Team</h1>

	<div class="card-container">
		<PresentationCard
      title="Facundo Lema"
      image="/images/facundolema.jpg"
      tags={['software developer', 'graphics designer']}
      cv="/cvs/facundolema.pdf"
      more="/facundolema"
      portfolios={[
        { name: 'Programming', link: '/facundolema/code'},
        { name: 'Photography', link: '/facundolema/photos'},
        { name: 'Design', link: '/facundolema/design'}
      ]}
    >
			Facundo is a software engineer who is passionate about music and technology.
		</PresentationCard>
		<PresentationCard
      title="Catalina Lettieri"
      image="/images/catalinalettieri.jpg"
      tags={['community manager']}
      cv="/cvs/catalinalettieri.pdf"
      more="/catalinalettieri"
      portfolios={[
        { name: 'Programming', link: '/catalettieri/code'},
        { name: 'Photography', link: '/catalettieri/photos'},
        { name: 'Design', link: '/catalettieri/design'}
      ]}
    >
			Facundo is a software engineer who is passionate about music and technology.
		</PresentationCard>
	</div>
</main>

<style>
	h1 {
		font-size: 4rem;
		font-weight: 600;
		font-family: 'Karla';
		margin: 0;
	}
	p {
		max-width: 40rem;
	}
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
