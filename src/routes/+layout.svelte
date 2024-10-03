<script>
	import githubLogo from '$lib/assets/images/github-mark.svg';
</script>

<header aria-label="Site Header">
	<a id="homeLink" href="/">OpenInvoice</a>
	<nav>
		<a href="/builder">Builder</a>
		<a href="https://github.com/nfowlie/open-invoice">
			<img src={githubLogo} alt="Github Project Link" />
		</a>
	</nav>
</header>

<slot />

<style>
	/*
      1. Use a more-intuitive box-sizing model.
    */
	:global(*),
	:global(*::before),
	:global(*::after) {
		box-sizing: border-box;
	}

	/*
        2. Remove default margin
      */
	:global(*) {
		margin: 0;
		-ms-overflow-style: none;
		/* IE and Edge */
		/* scrollbar-width: none; */
		/* Firefox */
	}

	:global(*::-webkit-scrollbar) {
		/* display: none; */
	}

	/*
        Typographic tweaks!
        3. Add accessible line-height
        4. Improve text rendering
      */
	:global(body) {
		line-height: 1.5;
		-webkit-font-smoothing: antialiased;
		height: 100vh;
		overflow: hidden;
		background-color: #f9fafb;
	}

	/*
        5. Improve media defaults
      */
	:global(img),
	:global(picture),
	:global(video),
	:global(canvas),
	:global(svg) {
		display: block;
		max-width: 100%;
	}

	/*
        6. Remove built-in form typography styles
      */
	:global(input),
	:global(button),
	:global(textarea),
	:global(select) {
		font: inherit;
	}

	/*
        7. Avoid text overflows
      */
	:global(p),
	:global(h1),
	:global(h2),
	:global(h3),
	:global(h4),
	:global(h5),
	:global(h6) {
		overflow-wrap: break-word;
	}

	/*
        8. Create a root stacking context
      */
	:global(#root),
	:global(#__next) {
		isolation: isolate;
	}

	/*
        9. Font Declaration
      */
	:global(*) {
		font-family:
			system-ui,
			-apple-system,
			BlinkMacSystemFont,
			'Segoe UI',
			Roboto,
			Oxygen,
			Ubuntu,
			Cantarell,
			'Open Sans',
			'Helvetica Neue',
			sans-serif;
	}

	:global(.button) {
		text-decoration: none;
		color: rgb(255, 255, 255);
		background-color: rgb(0, 0, 0);
		border-radius: 50px;
		padding: 0.5rem 1.25rem;
		font-size: 1.1rem;
		font-weight: 600;
	}

	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		font-size: 1.25rem;
		border-block-end: 2px solid rgb(243, 244, 246);
		padding-inline: 0.75rem;
		height: 3.5rem;
	}

	header a {
		text-decoration: none;
		color: inherit;
	}

	#homeLink {
		font-size: 1.25rem;
		font-weight: 700;
	}

	nav {
		display: flex;
		align-items: center;
		font-size: 0.85rem;
	}

	nav > a {
		margin-inline-start: 0.25rem;
		padding: 0.5rem 1rem;
		border-radius: 10px;
		color: rgb(107, 114, 128);
	}

	nav > a:hover {
		background-color: rgb(243 244 246);
	}

	nav > a > img {
		height: 1.5rem;
	}

	:global(main) {
		height: calc(100vh - 3.5rem);
	}
</style>
