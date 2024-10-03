<script>
	import { DateTime } from 'luxon';
</script>

<main>
	<section id="invoiceEditor">
		<div class="invoice-block">
			<label for="invoice-number">
				Invoice Number
				<input name="invoice-number" placeholder="INVOICE #0001" />
			</label>

			<label for="name">
				Name
				<input name="name" placeholder="Name" type="text" />
			</label>

			<label for="address-line-1">
				Address Line 1
				<input name="address-line-1" placeholder="Address Line 1" type="text" />
			</label>

			<label for="address-line-2">
				Address Line 2
				<input name="address-line-2" placeholder="Address Line 2" type="text" />
			</label>

			<label for="city">
				City
				<input name="city" placeholder="City" type="text" />
			</label>

			<label for="state">
				State
				<input name="state" placeholder="State" type="text" />
			</label>

			<label for="zip-code">
				Zip Code
				<input name="zip-code" placeholder="Zip Code" type="text" />
			</label>

			<label for="country">
				Country
				<input name="country" placeholder="Country" type="text" />
			</label>

			<label for="email">
				Email
				<input name="email" placeholder="hello@example.com" type="email" />
			</label>

			<label for="phone">
				Phone
				<input name="phone" placeholder="+1 (123) 456-7890" type="text" />
			</label>

			<label for="date">
				Date
				<input name="date" placeholder={DateTime.now().toFormat('LLLL dd, yyyy')} type="text" />
			</label>
		</div>
		<div class="invoice-block">
			<h2>Bill To</h2>

			<label for="name">
				Name
				<input name="name" placeholder="Name" type="text" />
			</label>

			<label for="address-line-1">
				Address Line 1
				<input name="address-line-1" placeholder="Address Line 1" type="text" />
			</label>

			<label for="address-line-2">
				Address Line 2
				<input name="address-line-2" placeholder="Address Line 2" type="text" />
			</label>

			<label for="city">
				City
				<input name="city" placeholder="City" type="text" />
			</label>

			<label for="state">
				State
				<input name="state" placeholder="State" type="text" />
			</label>

			<label for="zip-code">
				Zip Code
				<input name="zip-code" placeholder="Zip Code" type="text" />
			</label>

			<label for="country">
				Country
				<input name="country" placeholder="Country" type="text" />
			</label>

			<label for="email">
				Email
				<input name="email" placeholder="hello@example.com" type="email" />
			</label>

			<label for="phone">
				Phone
				<input name="phone" placeholder="+1 (123) 456-7890" type="text" />
			</label>
		</div>
	</section>
	<section id="invoicePreview">
		<div class="invoice"></div>
	</section>
</main>

<style>
	main {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 3rem;
		margin-inline: 1rem;
	}

	#invoiceEditor,
	#invoicePreview {
		overflow-y: scroll;
		display: grid;
		gap: 2rem;
		padding-inline-end: 2rem;
		padding-block: 2rem;
	}

	#invoiceEditor {
		justify-content: end;

		.invoice-block {
			background-color: #fff;
			padding: 1.25rem;
			border-radius: 8px;
			box-shadow:
				rgba(50, 50, 105, 0.15) 0px 2px 5px 0px,
				rgba(0, 0, 0, 0.05) 0px 1px 1px 0px;

			display: grid;
			grid-template-columns: 1fr 1fr;
			gap: 0.8rem;
			width: min(100%, 700px);

			label {
				display: grid;
				gap: 0.25rem;
				grid-column: span 2;
			}

			label[for='city'],
			label[for='zip-code'],
			label[for='email'] {
				grid-column: 1;
			}
			label[for='state'],
			label[for='country'],
			label[for='phone'] {
				grid-column: 2;
			}

			input {
				border-radius: 5px;
				outline: 2px solid transparent;
				outline-offset: 2px;
				border-color: rgb(209 213 219);
				border-width: 1px;
				box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
				padding-inline: 0.75rem;
				padding-block: 0.5rem;
				width: 100%;
			}
		}
	}

	#invoicePreview {
		justify-content: start;

		.invoice {
			aspect-ratio: 8.5/11;
			box-shadow:
				rgba(50, 50, 105, 0.15) 0px 2px 5px 0px,
				rgba(0, 0, 0, 0.05) 0px 1px 1px 0px;
			height: 700px;
			background-color: #fff;
		}
	}
</style>
