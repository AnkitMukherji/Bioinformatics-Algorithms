# Bioinformatics Algorithms: From Sequence Patterns to Genome Assembly

Python notebook implementations of core bioinformatics algorithms, organized around biological questions: locating replication origins, discovering regulatory motifs, and assembling genomes.

## Folder guides

- [Assembling Genomes](Assembling%20Genomes/README.md)
- [Molecular Clock](Molecular%20Clock/README.md)
- [Origin of Replication](Origin%20of%20Replication/README.md)

## Explore the collection

| Biological question | Methods and notebooks |
| --- | --- |
| Where might replication begin? | [Origin of Replication](Origin%20of%20Replication/): k-mer counts, reverse complements, Hamming distance, approximate matching, clump finding, and GC skew |
| Which sequence motifs recur? | [Molecular Clock](Molecular%20Clock/): motif enumeration, median strings, profile-based search, greedy/randomized search, and Gibbs sampling |
| How can reads reconstruct a genome? | [Assembling Genomes](Assembling%20Genomes/): overlap/de Bruijn graphs, Eulerian walks, paired-read reconstruction, and contig generation |

Reusable algorithm notebooks are at the root: [replication origin functions](replication_ori_functions.ipynb), [motif functions](motifs_to_find_molecular_clocks_functions.ipynb), and [assembly functions](how_do_we_assemble_genomes_functions.ipynb). Topic directories include problem notebooks and example input/output files.

## Working with the notebooks

Use Python with Jupyter. Inspect [pyproject.toml](pyproject.toml) and [requirements.txt](requirements.txt) for the recorded dependency configuration, create an isolated environment, and open notebooks from the repository root so relative paths resolve.

Run the relevant function cells before the problem cells. Compare outputs with the supplied examples, and record random seeds when evaluating stochastic searches. This is an educational implementation collection rather than a packaged command-line application.

## Connecting computation with biology

Sequence composition can suggest a replication-origin candidate, but it does not validate an origin experimentally. A high-scoring motif requires evaluation against an appropriate background. Assembly graphs make repeats and ambiguous reconstruction explicit; a path through a toy graph is not evidence of a complete biological genome.

The collection demonstrates algorithm construction and reasoning about search space, stochastic optimization, graph structure, and biological assumptions.

Related: [DNA sequencing algorithms](https://github.com/AnkitMukherji/Algorithms-for-DNA-Sequencing) · [Python sequence programming](https://github.com/AnkitMukherji/Python-for-Genomics).
