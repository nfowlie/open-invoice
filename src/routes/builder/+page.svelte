<script>
	import InvoiceEditor from '$lib/components/InvoiceEditor.svelte';
	import Invoice from '$lib/components/Invoice.svelte';
</script>

<main>
	<InvoiceEditor />
	<Invoice />
</main>

<style>
	main {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 3rem;
		margin-inline: 1rem;
	}

	:global(main > *) {
		overflow-y: scroll;
		display: grid;
		gap: 2rem;
		padding-inline-end: 2rem;
		padding-block: 2rem;
	}
</style>
