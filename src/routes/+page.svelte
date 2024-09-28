<main>
	<section id="hero">
		<div>
			<h1>Create a professional invoice easily</h1>
			<p>With this free open-source invoice builder</p>
			<div class="create">
				<a class="button" href="/builder">Create Invoice</a>
				<p class="disclaimer">No sign up required</p>
			</div>
		</div>
		<div></div>
	</section>
</main>

<style>
	main {
		margin-block: 2rem;
		margin-inline: 3rem;
	}
	#hero {
		display: grid;
		grid-template-columns: 1fr 1fr;

		h1 {
			font-size: 3rem;
			line-height: 1em;
			margin-block-end: 1rem;
			text-wrap: balance;
			word-break: keep-all;
		}

		p {
			font-size: 1.25rem;
		}
		.create {
			margin-block-start: 3rem;
		}

		.button::after {
			content: ' →';
		}

		.disclaimer {
			font-size: 1rem;
			color: rgb(75, 85, 99);
			margin-block-start: 1rem;
			margin-inline-start: 1.1rem;
		}
	}

	@media (max-width: 730px) {
		#hero {
			grid-template-columns: 1fr;

			align-items: center;
			text-align: center;

			h1 {
				font-size: 2.5rem;
			}

			.disclaimer {
				margin-inline-start: 0;
			}
		}
	}
</style>
