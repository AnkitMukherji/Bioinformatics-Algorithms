# Molecular-Clock
<b><i>Definitions of functions used:</i></b>

1. <b><i>MotifEnumeration</i></b>: Brute force algorithm to find motifs of length <b>k</b> with at most <b>d</b> mismatches in all strings in <b>Dna</b> by generating a neighborhood of motifs using the <b>Neighbors</b> function.

2. <b><i>entropy</i></b>: Calculates the entropy of a motif matrix. It scores individual instances of motifs depending on how similar they are to a consensus.

3. <b><i>DistanceBetweenPatternAndStrings</i></b>: Calculates the sum of minimum Hamming distances between a pattern and a collection of strings.

4. <b><i>median_string_all_kmers</i></b>: Solves the Median String Problem by checking all possible $4^k$ k-mers to find one that minimizes the distance to a collection of strings.

5. <b><i>all_kmers_from_dna</i></b>: Extracts all k-mers present in a given collection of DNA strings.

6. <b><i>median_string_kmers_from_dna</i></b>: An optimized version of the Median String Problem that only checks k-mers actually present in the DNA strings.

7. <b><i>profile_probability</i></b>: Calculates the probability of a specific k-mer based on a given profile matrix.

8. <b><i>profile_most_probable_kmer</i></b>: Finds the k-mer in a sequence that has the highest probability according to a given profile matrix.

9. <b><i>form_profile</i></b>: Generates a profile matrix from a list of motifs (frequencies of each nucleotide at each position).

10. <b><i>score_motifs</i></b>: Calculates the score of a list of motifs, measuring how conserved they are by counting non-consensus nucleotides.

11. <b><i>greedy_motif_search</i></b>: An iterative algorithm that builds a profile matrix one sequence at a time to find the best conserved motifs.

12. <b><i>form_profile_pseudocounts</i></b>: Creates a profile matrix using <b>Laplace's Rule of Succession</b> (adding 1 to each count) to avoid zero probabilities.

13. <b><i>greedy_motif_search_pseudocounts</i></b>: Improved version of the greedy search that uses pseudocounts for more robust motif finding.

14. <b><i>Random_Motifs</i></b>: Generates a set of initial motifs by randomly picking a k-mer from each DNA sequence.

15. <b><i>Generate_Motifs</i></b>: Generates new motifs based on a profile matrix and a set of DNA sequences.

16. <b><i>Score</i></b>: Calculates the score of a set of motifs based on the consensus sequence.

17. <b><i>Randomized_Motif_Search</i></b>: A randomized approach combined with iterative improvement to converge on a set of conserved motifs.

18. <b><i>Run_Randomized_Motif_Search</i></b>: Runs the randomized search multiple times with different random starts to find the global optimum.

19. <b><i>ProfileRandomlyGeneratedKmer</i></b>: Generates a k-mer from a sequence based on a probability distribution derived from a profile matrix (used in Gibbs Sampling).

20. <b><i>GibbsSampler</i></b>: A Markov Chain Monte Carlo (MCMC) algorithm that iteratively updates one motif at a time to find hidden motifs.

21. <b><i>runGibbsSampler</i></b>: Runs the Gibbs Sampler multiple times to ensure convergence to the best motif set.

<br>

<b><i>Problems & Usage:</i></b>
The <b><i>motifs_to_find_molecular_clocks_problems.ipynb</i></b> notebook applies these algorithms to find conserved patterns (motifs) in biological sequences, including:
*   Finding motifs in regulatory sequences like the <b><i>Mycobacterium tuberculosis</i> DosR</b> regulon.
*   Calculating entropy for motifs such as those associated with <b>NF-κB</b>.
*   Solving the <b>Median String Problem</b> to find the most representative k-mer in a set of sequences.
*   Comparing <b>Greedy</b>, <b>Randomized</b>, and <b>Gibbs Sampling</b> approaches for motif discovery.

## Notebook

[motifs_to_find_molecular_clocks_problems.ipynb](motifs_to_find_molecular_clocks_problems.ipynb) contains the worked exercises. Works through motif enumeration, profile and entropy calculations, and deterministic and randomized motif searches. Open it from a working directory that resolves the exercise input files referenced in its cells.
