<script>
	import { PDFDocument, StandardFonts, rgb } from 'pdf-lib';
	import PDFObject from 'pdfobject';
	import { invoiceRune } from './InvoiceRune.svelte';
	import { watch } from 'runed';

	async function createPdf() {
		const pdfDoc = await PDFDocument.create();
		const page = pdfDoc.addPage();

		const timesRomanFont = await pdfDoc.embedFont(StandardFonts.TimesRoman);

		const { width, height } = page.getSize();
		const fontSize = 30;

		page.drawText(invoiceRune.invoiceNumber, {
			x: 50,
			y: height - 4 * fontSize,
			size: fontSize,
			font: timesRomanFont,
			color: rgb(0, 0, 0)
		});

		const pdfBytes = await pdfDoc.save();
		const blob = new Blob([pdfBytes], { type: 'application/pdf' });

		const pdfPreview = window.URL.createObjectURL(blob);

		const pdfOptions = {
			title: 'Invoice',
			pdfOpenParams: { view: 'Fit' },
			height: '100%',
			width: '100%'
		};

		PDFObject.embed(pdfPreview, '#invoice', pdfOptions);
	}

	watch(
		() => invoiceRune.invoiceNumber,
		async () => {
			await createPdf();
		}
	);
</script>

<section id="invoicePreview">
	<div id="invoice"></div>
</section>

<style>
	#invoicePreview {
		justify-content: start;

		#invoice {
			aspect-ratio: 8.5/11;
			box-shadow:
				rgba(50, 50, 105, 0.15) 0px 2px 5px 0px,
				rgba(0, 0, 0, 0.05) 0px 1px 1px 0px;
			height: 700px;
			background-color: #fff;
		}
	}
</style>
