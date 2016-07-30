# PuFFIN
A Parameter-free Method to Build Genome-wide Nucleosome Maps from Paired-end Sequencing Data

Dowload


Input

The input file for the tool should contain the reads only for one chromosome (or a contig) and is in a BED format obtained by simply parsing the BAM/SAM file (see bam2bedpe.sh for example).

Usage

Given that input reads are in input.bam, that contain only reads for particular chromosome

./bam2bedpe.sh input.bam > input.bed
python Run.py input.bed

The output will be printed in input.bed.nucs using next column format:
<Position of the nucleosome center> <width of the peak> <confidence score> <"Fuzziness"> <Level of the curve that was used to detect nucleosome >
