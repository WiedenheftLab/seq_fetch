# seq_fetch

Author: Murat Buyukyoruk

Associated lab: Wiedenheft lab

# seq_fetch help:

This script is developed to fetch sequences from multifasta file by using a list of accession numbers to fetch. 

SeqIO package from Bio is required to fetch sequences. Additionally, tqdm is required to provide a progress bar since some multifasta files can contain long and many sequences.
        
Syntax:

    python seq_fetch.py -i demo.fasta -l demo_sub_list.txt -o demo_sub_list.fasta

seq_fetch dependencies:

    Bio module and SeqIO available in this package      refer to https://biopython.org/wiki/Download
    tqdm                                                refer to https://pypi.org/project/tqdm/
	
Input Paramaters (REQUIRED):
----------------------------
	-i/--input		FASTA			Specify a fasta file. FASTA file requires headers starting with accession number. (i.e. >NZ_CP006019 [fullname])

	-l/--list		List			Specify a list of accession (Accession only). Each accession should be included in a new line (i.e. generated with Excel spreadsheet). Script works with or without '>' symbol before the accession.

	-o/--output		Output file	        Specify a output file name that should contain fetched sequences.
	
Basic Options:
--------------
	-h/--help		HELP			Shows this help text and exits the run.
  
# Note:
Demo files are available to use with the basic command line provided in syntax section above. Make sure all the dependencies are installed successfully to the python environment.

    demo.fasta          Includes 8 genome sequences
    demo_sub_list.txt   Inludes list of accessions w/o '>' symbol. It is okay to have '>' symbol in the begining of the accession (i.e. '>NZ_CP006019')
