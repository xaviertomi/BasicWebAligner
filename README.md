# BWA — Basic Web Aligner

**Basic Web Aligner (BWA)** is a lightweight web tool for pairwise nucleotide sequence alignment.

It runs entirely in the browser and requires no installation, backend, or server.

## Features

- Pairwise nucleotide sequence alignment
- FASTA input
- Runs locally in the browser
- No sequence upload to an external server
- Colored nucleotide visualization
- Full FASTA sequence names displayed
- Navigation between gap groups
- Alignment statistics
- FASTA export
- Affine gap penalties for long insertions and deletions

## Alignment method

BWA performs a global pairwise alignment using affine gap penalties.

Affine gap penalties distinguish between opening a new gap and extending an existing one. This helps represent long insertions or deletions as a single continuous gap instead of multiple small gaps separated by isolated matches.

Default scoring:

```text
Match       +2
Mismatch    -3
Gap open    -10
Gap extend  -0.5
```

The scoring parameters can be modified directly in the interface.

## Usage

Open the HTML file in a modern web browser.

Paste two FASTA sequences into the input box:

```fasta
>sequence_1
ACTGACCTGATCGATCGATC

>sequence_2
ACTGACCTGAAAAATCGATCGATC
```

Then start the alignment.

The aligned sequences are displayed with nucleotide coloring and alignment statistics.

## Gap navigation

Contiguous gaps are grouped together.

The **Previous gap group** and **Next gap group** buttons allow quick navigation between distinct insertion/deletion regions.

## Privacy

All sequence processing is performed locally in the browser.

No sequence data is sent to an external server.

## Limitations

BWA is intended for relatively small pairwise sequence comparisons.

It is not intended for:

- whole-genome alignment
- read mapping
- multiple sequence alignment
- high-throughput sequence analysis

## Running locally

No installation is required.

Simply download the HTML file and open it:

```bash
firefox basic_web_aligner.html
```

or open it directly from your file explorer.

## License

Add your preferred license here.
