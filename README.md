# Lab2_sanger_sequencing

## Getting Started
1. Download Example Sanger sequences to a folder on your desktop (see Note 5.1).
• https://www.vanderbilt.edu/wolbachiaproject/lab-5-dna-sequences/
2. Download SnapGene Viewer to your computer:
• https://www.snapgene.com/snapgene-viewer/
3. Open SnapGene Viewer.


## Edit the Forward Trace File

4. Select Open >> Open Files >> Example1-WSpecF.ab1.
5. Select File >> Save As >> Mod.WSpecF.scf (or name of your preference). Rename the sequence to create a copy of the original .ab1 file (See Note 5.2). Since SnapGene Viewer does not have an .ab1 option, use the comparable .scf extension.
6. Select “Show quality values” in the lower right hand corner. The bars correlate to quality score. Hover the cursor over each bar to visualize the quality score.

NOTE: Always make a copy of raw data prior to editing. Keep the originals in case you make a mistake along the way or need to refer to the raw sequences in the future.

<img width="863" alt="Screen Shot 2025-01-19 at 3 26 23 PM" src="https://github.com/user-attachments/assets/4e644e82-3c7a-4739-a270-53c5b0272863" />


7. Use the bottom scroll bar to scan the sequence. Confirm that the majority of the sequence contains unique peaks with quality values ≥ 40.
8. The ends of the sequence will likely be low-quality (as seen above). Therefore, it is necessary to trim/delete poor base calls. Beginning at the 5’-end (left), identify the beginning of the “high quality sequence”.
9. Using the cursor, highlight ALL bases prior to this sequence. For this example, we will apply the most conservative guidelines and select for the contiguous sequence with ≥ 40 quality scores. Therefore, we will trim the first 54 bases.
10. Hit ‘Delete.’ ONLY trim from the ends, not the interior portion of the sequence!
11. Repeat steps #7-9 for the 3’-end (right). Applying the most conservative guideline, we will trim the last 17 bases.
12. Scroll through the sequence. Are all quality scores ≥ 40? If there is a low-value base call in the middle of the sequence, DO NOT DELETE. Use your judgment here. Does the peak look unique? Is the value near 40 (i.e., 37-39)? If yes, you can leave as is. If you are not confident with this base call, highlight with your cursor and type ‘N’. This will replace the base call with ‘N’, indicating that the exact base is unknown.
13. Select File >> Export >> FASTA Format.
14. Check your folder. You should now have 3 files for this sequence: the original trace file (.ab1), the modified trace file (.scf), and the FASTA file.

## Edit the Reverse Trace File – repeat the same steps from the forward file

15. In SnapGene Viewer, select Open >> Open Files >> Example2-WSpecR.ab1.
16. Select File >> Save As >> Mod.WSpecR.scf (or name of your preference).
17. Select “Show quality values” in the lower right hand corner.
18. Use the bottom scroll bar to scan the sequence. Confirm that the majority of the sequence
contains unique peaks with quality values ≥ 40.
19. Beginning at the left, identify the beginning of the “high quality sequence.”
20. Using the cursor, highlight ALL bases prior to this sequence.
21. Hit ‘Delete.’
22. Repeat steps #19-21 for the right end of the sequence.
23. Scroll through the sequence. Are all quality scores ≥ 40?
24. Select File >> Export >> FASTA Format.
25. Check your folder. You should now have 3 files for this sequence: the original trace file (.ab1), the modified trace file (.scf), and the FASTA file.

## Generate a Consensus Sequence

26. Open NCBI in your web browser: https://www.ncbi.nlm.nih.gov/
27. Select “BLAST” from the right-hand ‘Popular Resources’ menu
28. Select “Nucleotide BLAST.”
29. (optional) Enter a Job Title.
30. Click “ Align two or more sequences” at the bottom of the first box.
31. Load your forward FASTA file in the top box and the reverse FASTA file in the second box. Hit BLAST.

• The lower box shows the alignment of the two sequences.

• Bases that are gray and lower case indicate low complexity regions.

33. Check the % Identity. It should be 100%. If not, refer back to the trace files and investigate the discrepancy.
34. If your identity is 100%, select the Arrow next to “Download” and download FASTA (aligned sequences). Save. You have now generated a Consensus Sequence. You will use this high quality DNA sequence in Part 2 of the Bioinformatics Lab.

## Analyze a “Less than Perfect” Sanger Sequence

34. In SnapGene Viewer, select Open >> Open Files >> Example3-HCO2198.ab1.
35. Select File >> Save As >> Mod.HCO2198.scf (or name of your preference).
36. Select “Show quality values” in the lower right hand corner. Notice the low Q scores.
37. Not only are Q scores < 40, but there are also multiple peaks for each base call.
• This is a low-quality sequencing run and base calls should not be trusted.
38. Open the complementary strand In SnapGene Viewer: select Open >> Open Files >> Example4-LCO1490.ab1.
39. Select File >> Save As >> Mod.LCO1490.scf (or name of your preference).
40. Select “Show quality values” in the lower right hand corner.
• This sequence is a better run and can be trusted.
41. Repeat steps 7-14 for this sequence.
42. You may use this sequence for downstream bioinformatics analyses, but note that the sequence was obtained from a single direction.
<img width="894" alt="Screen Shot 2025-01-19 at 3 40 50 PM" src="https://github.com/user-attachments/assets/956796bd-3ed3-4da7-8e66-f22531f1677c" />

