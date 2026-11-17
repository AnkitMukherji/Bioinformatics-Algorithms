# Origin-of-Replication
<b><i>Definition of the functions used:</i></b>

1. <b><i>PatternCount</i></b>: Program to check how many times a <b>Pattern</b> appears in a <b>Text</b>.

2. <b><i>FrequentWords</i></b>: Program to find the most frequent kmers of length <b>k</b> appearing in <b>Text</b>.

3. <b><i>HanoiTowers</i></b>: A mathematical puzzle in which we have to move all the disks from Tower 1 to Tower 3 but we cannot place a larger disk onto a smaller disk. This is a classic recursion problem.

4. <b><i>SymbolToNumber</i></b>: Converts a DNA symbol (A, C, G, T) to its corresponding numeric code.

5. <b><i>PatternToNumber</i></b>: Program to convert a pattern into a number. This calculates the 0-based index position of the pattern if we generate all kmers of the length of the pattern and sort them lexicographically.

6. <b><i>NumberToSymbol</i></b>: Converts a numeric code back to its DNA symbol.

7. <b><i>NumberToPattern</i></b>: Program to convert a number into a kmer pattern. It treats each DNA base as a digit. The number is repeatedly divided by 4 to determine each position's symbol from right to left.

8. <b><i>ComputingFrequencies</i></b>: Computes the frequency array for all possible k-mers in a text.

9. <b><i>FasterFrequentWords</i></b>: Finds most frequent k-mers using frequency arrays for efficiency.

10. <b><i>FindingFrequentWordsBySorting</i></b>: Finds most frequent k-mers by sorting k-mer occurrences.

11. <b><i>ReverseComplement</i></b>: Program to find the reverse complement of a <b>DNA</b> string.

12. <b><i>ReverseComplement2</i></b>: An alternative implementation for finding the reverse complement using a dictionary mapping.

13. <b><i>PatternMatching</i></b>: Program to find all the starting positions of the <b>Pattern</b> in the <b>Genome</b>.

14. <b><i>ClumpFinding</i></b>: We can define a k-mer as a "clump" if it appears many times within a short interval of the genome. A k-mer pattern of length <b>k</b> forms an <b>(L, t)</b> clump inside a longer string Genome <b>(Text)</b> if there is an interval of Genome of length L in which this k-mer appears at least t times.

15. <b><i>BetterClumpFinding</i></b>: Works similarly to <b>ClumpFinding</b> but more efficient. Instead of recounting from scratch for each window, it updates counts by removing the first k-mer that leaves the window and adding the new k-mer that enters. This narrows down the search process.

16. <b><i>MinimumSkewProblem</i></b>: Finds positions in a genome with the minimum skew (difference between G and C counts). This is useful for identifying the origin of replication (ori).

17. <b><i>HammingDistance</i></b>: Program to find the number of mismatches (position wise) between two strings of equal length.

18. <b><i>ApproximatePatMatch</i></b>: Program to find all starting positions where <b>Pattern</b> appears as a substring of <b>Text</b> with atmost <b>d</b> mismatches.

19. <b><i>immediate_neighbors</i></b>: Generates all k-mers differing by exactly one mismatch from a given pattern.

20. <b><i>Neighbors</i></b>: Program to generate the set of all k-mers whose <b>Hamming distance</b> from <b>Pattern</b> does not exceed <b>d</b>.

21. <b><i>ExactNeighbors</i></b>: Finds patterns that are exact neighbors (distance exactly d) of a given pattern.

22. <b><i>IterativeNeighbors</i></b>: Generates neighbors iteratively by extending mismatches.

23. <b><i>FrequentWordsWithMismatches</i></b>: Finds most frequent k-mers with up to d mismatches in a text.

24. <b><i>FindingFrequentWordsWithMismatchesBySorting</i></b>: A faster algorithm to find frequent words with mismatches by sorting neighborhood arrays.

25. <b><i>FindingFrequentWordsWithMismatchesBySortingAndReverseComplements</i></b>: Finds most frequent k-mers with mismatches considering both the pattern and its reverse complement.

26. <b><i>FrequentWordsWithMismatchesAndReverseComplements</i></b>: A faster algorithm to find frequent words with mismatches and reverse complements using a hash map (defaultdict).

<br>

<b><i>Problems & Usage:</i></b>
The <b><i>replication_ori_problems.ipynb</i></b> notebook contains implementations and solutions to various problems related to finding the Origin of Replication, including:
*   Finding frequent words and clumps in the <b><i>E. coli</i></b> genome.
*   Generating skew diagrams for <b><i>E. coli</i></b> and <b><i>Salmonella enterica</i></b> to locate <i>oriC</i>.
*   Solving the <b>Minimum Skew Problem</b> to identify potential replication origins.
*   Finding approximate matches and frequent words with mismatches in genomic sequences.

## Notebook

[replication_ori_problems.ipynb](replication_ori_problems.ipynb) contains the worked exercises. Uses k-mer search, mismatch counts, reverse complements, clumps and skew to explore replication-origin signals. Open it from a working directory that resolves the exercise input files referenced in its cells.
