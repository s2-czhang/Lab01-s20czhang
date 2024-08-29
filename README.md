# Lab1 - Introduction to Gene Exploration and GitHub

**Note: This lab is copyrighted by Joshua Rest. Do not post any part of it online.**

## Part I. Introduction and Working with GitHub and markdown.

## Structure of Labs

Throughout this semester, you will acquire the skills to compare gene families present in various bilaterian animals. The lectures will provide you with the necessary background knowledge about biology and analysis tools. In each lab session, we will collectively work on a common gene family. Additionally, you will conduct independent analysis on a gene family that we will assign you. These lab sessions will serve as the basis for your final research paper on the selected gene family.

Instructions and commands for each lab will be provided on GitHub. You will create a repository for each lab using a template, just like you did in today's lab. The README document will outline the analysis tasks for the lab on "GLOBINS". You are required to post your answers to questions both on <img src="img/github.png" alt= “” width="20" height="20">[GitHub] and <img src="img/brightspace.png" alt= “” width="20" height="20">[Brightspace]. Furthermore, you should document any commands, calculations, or code you run in your repository. It is recommended to use the markdown editor in VS Code to edit your repository files. Your repositories will be checked five times during the semester.

## Keeping Track of Work on GitHub

- GitHub is a commercial platform that hosts code repositories and facilitates collaboration among developers.
- It is based on Git, a version control system that records changes made to code documents.
- GitHub allows you to check out or create a fork (a separate version) of code, enabling collaborative work.
- Familiarize yourself with GitHub by referring to the following resources:
    - [What is GitHub?](https://kinsta.com/knowledgebase/what-is-github/)
    - [GitHub Hello World Guide](https://guides.github.com/activities/hello-world/)
    - [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

### Git and Version Control

- Git is a distributed version control system that enables collaboration on projects.
- It tracks changes to files and directories, providing the ability to revert to previous versions if necessary.
- Git facilitates seamless collaboration among developers by allowing simultaneous work on different project parts and merging changes together.

### GitHub Features and Usage

- GitHub is a web-based hosting service for Git repositories.
- It offers features such as issue tracking, project management, and pull requests.
- Developers can store their Git repositories on GitHub, making it easy to collaborate with others.
- GitHub is commonly used for writing, sharing, and collaborating on code.
- Create a GitHub account with the username `<s#-netid>`, where `<s#>` represents your lab section number and `<netid>` is your identifier. Examples: s1-cdarwin, s2-cdarwin, s3-cdarwin, s4-cdarwin, s5-cdarwin. NOTE: please do not use s01 for section 1, use s1.
- Generate a Personal Access Token (PAT) for accessing your GitHub account from other machines. Follow these steps:
    1. Open your web browser and go to: https://github.com/settings/tokens
    2. Click on "Generate new token."
    3. Add a note (e.g., for BIO-312).
    4. Select an expiration date (ensure it lasts until the end of the semester).
    5. Check the "repo" box under scopes.
    6. Click on "Generate token."
    7. **Copy and securely save your token for future labs.**

### Editing Markdown Files in VS Code

1. Download the file by clicking on it and selecting the download button.
2. You could open this file directly with a simple text editor like Windows::Notepad or MacOS::TextEdit. We recommend using Visual Studio Code, a source-code editor.
3. Download and install Visual Studio Code from this [link](https://code.visualstudio.com/).
4. Install the "Markdown Preview Enhanced" extension in Visual Studio Code.
5. Open a Markdown file (.md) in Visual Studio Code.
6. Use the "Markdown: Open Preview to the Side" option from the Command Palette (Ctrl+k v or Cmd+k v on macOS) to view the Markdown preview alongside the code.

### Lab Completion and Submission

- While completing the lab tasks, answer the brightspace questions and upload a copy of your edited README.md markdown file in your lab repository for grading.

## Part II. Gene Exploration at NCBI

NCBI (National Center for Biotechnology Information) hosts a website where biologists store and retrieve information about genes, genomes, and other biological data. As we progress in this course, NCBI will become your go-to resource. NCBI consists of multiple databases, each focusing on different aspects of genes, genomes, or proteins.

The objective of today's lab is to familiarize ourselves with the structure of a gene and how we can retrieve information about a gene from NCBI. Throughout this semester, we will study not only this particular gene but also its gene family.

In today's lab, we will explore the GenBank files describing the sequence of the gene cytoglobin-1, coelomic-like (LOC100375093) from the species *Saccoglossus kowalevskii* (an acorn worm, class/order Enteropneusta, phylum Hemichordata).

To find a summary of the information available for this gene, visit the [NCBI Gene page](http://www.ncbi.nlm.nih.gov/gene) and enter the gene ID 100375093 in the search box. The gene page provides a graphical view of the scaffold, where you can see the location of the gene within the genome. It also provides basic information such as gene name, symbol, description, and other relevant details.

### Explore the genomic context of a gene

1. Visit the [NCBI Gene page](http://www.ncbi.nlm.nih.gov/gene) and search for the gene ID 100375093.

2. Explore the information available on the gene page.

Look down on the gene page, and you will see a  graphical view of the scaffold and Genomic DNA. The gene is annotated below the scaffold:
![Gene View](img/Fig1.png)

Please note that there could be multiple transcript variants shown, but that is not applicable to this gene. 
Think, discuss, and look up: what is a transcript variant? 
Think, discuss, and look up: What is an isoform?

3. Take a look at the GenBank format of the gene, which includes information on its location on the scaffold. To get to the GenBank format file, click here:
![Genbank format file of this gene](img/genbank_view.png)

Here is what the Genbank format file looks like:
![Region of our gene](img/Fig2.png)

Genes can be occasionally listed on a scaffold in draft genomes where DNA chunks aren't fully assembled into chromosomes. Note that you're currently viewing the partial section of a scaffold38908 containing the gene LOC100375093.

The selected region is:
```
complement(209977..232793)
```
Discuss or look up what the term "scaffold" means.
Discuss or look up what it means that this gene is encoded on the complementary strand.

You can also see the length of this region:
```
22817 bp
```
Now, to see the entire scaffold, change the view to "whole sequence".

![Change Region Shown](img/Fig3.png)

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub]  Make notes for yourself here about how you figured out the length of the entire scaffold. Use the editor to directly edit the markdown file. 

I changed the region shown to show the whole sequence. From here, I looked at the number of base pairs given in the locus section

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace]  1. What is the length of the **entire** scaffold?

```result
the length of the entire scaffold is 1030712 base pairs
```

### Retrieving the GenBank File

Return again to the GenBank file for the Genomic DNA of the gene LOC100375093 (cytoglobin-1). This time, we will download the Genbank:
Save the Genbank file by clicking on "Send to" (to the left of "Change Region Shown"), choose the destination "File", and select the GenBank format.

### Examining the GenBank File

Open the downloaded GenBank file using VS Code. The GenBank file follows a specific format and contains various sections that provide information about the gene and its associated features. (Note: you can also examine the Genbank entry in the browser.)

Examine the contents of the GenBank file, paying attention to the following sections:

- LOCUS: Provides general information about the sequence, including its length and other basic details.
- DEFINITION: Describes the gene and its function in more detail.
- FEATURES: Lists the features and annotations associated with the gene, such as coding sequences, exons, and other important elements.
- ORIGIN: Presents the nucleotide sequence of the gene.

Take some time to explore the different sections of the GenBank file and familiarize yourself with the information they provide.


Find the **annotation of coordinates for the mRNA of the gene** within this region.  Specifically, the coordinates for the exons are provided by “join(…)”. Note the coordinates of the coding sequence (CDS) are also provided. You will need to compare the coordinates for the mRNA to the coordinates for the CDS to answer this question.

This is what is looks like:
```
     mRNA            join(1..346,16217..16442,22064..22817)
                     /gene="LOC100375093"
                     /product="cytoglobin-1-like"
```

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 2. How many exons are there that make up the mRNA for LOC100375093 (cytoglobin-1)? How many introns are there in the Genomic DNA, that are removed in the mature mRNA? 

There are 3 exons. As for the introns, there are 2 introns.

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Make notes here about how you answered the question.

To find out the number of exons, I counted the number of intervals included in the join() in the mRNA section. In this case, since there are 3 intervals, I conclude that there are 3 exons. Meanwhile, for the number of introns, I just counted the number of spaces between each exons, up to the end of this gene sequence. This ends up being only 2 introns.

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 3. What are the lengths of each of the first three exons for LOC100375093 (cytoglobin-1)? The length of the second exon is calculated for you.  

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Fill in your own calculations below.
```result
Exon 1: 346 - 0 = 346 bp
Exon 2: 16442-16216 = 226 bp
Exon 3: 22817 - 22063 = 754 bp
```
> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 4. What are the lengths of each of the first two introns of LOC100375093 (cytoglobin-1)? The length of the first intron is calculated for you.

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Fill in your own calculations below.
```result
Intron 1: 16216 - 346 = 15870 bp
Intron 2: 22063 - 16442 = 5621 bp
```
> [Brightspace] 5. What is the total length of the mRNA for LOC100375093 (cytoglobin-1)?

The total length of the mRNA is 1326 bp

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Show your calculations or notes below.**
*Hint: You could add up the length of all the exons, or you could navigate to the  mRNA molecule in Genbank.*
```result                   
total length = 346 + 226 + 754
total length = 572 + 754
total length = 1326
```

mRNA contains a 5’ UTR, the coding sequence, and a 3’ UTR. To calculate the length of the UTRs, we need to compare the mRNA to the CDS. To find the annotation for the coding sequence of LOC100375093 (cytoglobin-1), scroll down to the following annotation:
```
     CDS             join(180..346,16217..16442,22064..22285)
                     /gene="LOC100375093"
```

><img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 6. What exon does the coding sequence start in for LOC100375093 (cytoglobin-1)?

The coding sequence starts in the first exon

><img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Show your notes here.  
```result
The CDS starts on the 180 bp, which falls between the interval of the first exon (1...346).
```

><img src="img/brightspace.png" alt= “” width="20" height="20">[Brightspace] 7. By comparing the coordinates of the mRNA and the CDS, calculate length of the 5’ UTR for LOC100375093 (cytoglobin-1). *Hint: the bases including the start of the mRNA and up to (but not including) the start of the CDS.*  
```result
The length of the 5' UTR is 179 bp
```

><img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 8. By comparing the coordinates of the mRNA and the CDS, calculate length of the 3’ UTR for LOC100375093 (cytoglobin-1). *Hint: the bases after (but not including) the end of the CDS (i.e. after the stop codon), until the end of the mRNA.*  
```result
The length of the 3' UTR is 532 bp
```
><img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Show your calculation here.

5' UTR: 179 - 0 = 179 bp
3' UTR: 22817 - 22285 = 532 bp
 
> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 9. What is the length of the coding sequence (CDS) in nucleotide base pairs (bp) for LOC100375093 (cytoglobin-1)?  

The length of the coding sequence is 615 bp

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Make notes here on how you solved the problem.
```result
first: 346 - 179 = 167 bp
second: 16442 - 16216 = 226 bp
third: 22285 - 22063 = 222 bp
total length = 167 + 226 + 222
total length = 393 + 222
total length = 615 
```

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 10. How many codons are in the coding sequence for LOC100375093 (cytoglobin-1)?
Hint: remember the **stop codon is a codon**, and it is included in the CDS.

There are 205 codons in the coding sequence

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Make notes here on how you solved the problem.
```result
# of codons = 615 / 3 
# of codons = 205
```

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 11. How many amino acids are in the protein cytoglobin-1 encoded for by LOC100375093? *Hint: the stop codon does not encode an amino acid.*   
```result
204
```
> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Make notes here on how you solved the problem.

Each codon encodes a single amino acid, except for the stop codon. So, I just subtracted 1 from the total codons, to get 204 codons. These codons encode amino acids, so there will be 204 amino acids in the resulting chain.

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 12. What are the first nine bases of the coding sequence (CDS) for LOC100375093 (cytoglobin-1)?  
```result
atgggatgc
```
Example format for your answer: NNNNNNNNN  
*Hint: An easy way to do this is to navigate to the mRNA page and click on "Highlight Features".*

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 13. What are the amino acids (single letter code) encoded by these nucleotides? Example format for your answer: XXX. [Translate tool](https://web.expasy.org/translate/)   
```result
MGC
```

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 14. Can you find the length of the introns from the mRNA and protein file? Why or why not? Recall that there are three different files we have looked at: (1) the genomic DNA file, (2) the mRNA file, (3) the protein file; review these files before answering the question.  Hint: The mRNA file always shows only fully spliced mRNA. Hint: The links to the proteins and mRNA files are named XM_ or XP_ under features.

No, because the mature mRNA will no longer include the introns. This means that from the mature mRNA, we will not be able to see the space where the introns were previously, and thus cannot count their lengths.

> <img src="img/github.png" alt= “” width="20" height="20"> [GitHub] Upload the GenBank file to your repository by clicking Add file.

> <img src="img/brightspace.png" alt= “” width="20" height="20"> [Brightspace] 15. Would it be possible for a CDS to have the start codon in a different exon other than exon 1?

Yes, it is possible

## Part III. A Gene has a Family

In order to determine the gene family to which cytoglobin-1(LOC100375093) belongs, we can employ various methods and references. The concept of a gene family can have multiple overlapping definitions, and understanding them will be an ongoing process throughout the semester. For now, let's focus on getting a starting point for our investigation.

Here is a suggested approach:

1. Begin by visiting scholar.google.com.
2. Enter the search query "cytoglobin globin family subfamily superfamily phylogeny" (without quotes).
3. Review the first two articles that appears. Please note that the gene from *Saccoglossus kowalevskii* may not be included in this article. However, we are specifically looking for any gene referred to as "cytoglobin-1" or "cygb-1" (or jus cytoglobin) as this will provide sufficient information to determine its family membership.

Another approach is to explore the NCBI page for the gene and examine the Conserved Domains section under the NCBI Reference Sequences (RefSeq). In this case, the annotation reveals "cl21461 Globin-like; Globin-like protein superfamily" which refers to the globin-like domain superfamily which contains a wide variety of all-helical proteins that bind porphyrins, phycobilins, and other non-heme cofactors. 

Next week, you will be assigned a gene family for your own term project. To start, you will have a *single gene* from that gene family. Then, you will figure out which gene family the gene belongs to.

Please commit your changes to the README file with all the questions labeled [GitHub] answered (you can copy-paste the md note from VS Code).
Also, make sure all the required files have been added to the repository. To end the lab review the Markdown Cheat Sheet below.

**Congratulations on completing Lab 1!**

# Markdown Cheat Sheet

This guide serves as a reference to some of the formatting options available in Markdown. Markdown is a lightweight markup language that allows you to format text documents in a simple and readable way. Use this cheat sheet to explore different Markdown features and enhance your documents.

# Markdown Cheat Sheet

Headers
---------------------------

# Header 1

## Header 2

### Header 3

Styling
---------------------------

*Emphasize*  _emphasize_

**Strong**  __strong__

==Marked text.==

~~Mistaken text.~~

> Quoted text.

H~2~O is a liquid.

2^10^ is 1024.

Lists
---------------------------

1. Bioinformatics Databases
   - GenBank
   - Protein Data Bank (PDB)
   - European Nucleotide Archive (ENA)
   - Universal Protein Resource (UniProt)
   - Kyoto Encyclopedia of Genes and Genomes (KEGG)

2. Sequence Analysis
   - Pairwise sequence alignment
     - Needleman-Wunsch algorithm
   - Multiple sequence alignment
     - MUSCLE
   - Sequence similarity search
     - Basic Local Alignment Search Tool (BLAST)

3. Data Visualization and Analysis
   - R programming language
     - ggplot2
     - Bioconductor
   - Python programming language
     - Matplotlib
     - Pandas
     - Biopython

   
- [ ] Incomplete item
- [x] Complete item

Links
---------------------------

A [link](http://www.ncbi.nlm.nih.gov).

An image: ![Alt](img.jpg)

A sized image: ![Alt](img.jpg =60x50)

Code
---------------------------

Some `inline code`.

```
// A code block
var foo = 'bar';
```

```bash
#!/bin/bash

# This is a simple Bash script
# It prints "Hello, World!" to the console

echo "Hello, World!"
```

Tables
---------------------------

| Organism      | Common Name          | Kingdom     | Phylum        | Class           |
| ------------- | -------------------- | ----------- | ------------- | --------------- |
| Homo sapiens  | Human                | Animalia    | Chordata      | Mammalia        |
| Mus musculus  | Mouse                | Animalia    | Chordata      | Mammalia        |
| Drosophila melanogaster | Fruit fly   | Animalia    | Arthropoda    | Insecta         |
| Arabidopsis thaliana   | Thale cress  | Plantae     | Angiosperms   | Eudicots        |
| Escherichia coli       | E. coli      | Bacteria    | Proteobacteria | Gammaproteobacteria |


| Column 1 | Column 2 |
|:--------:| -------------:|
| centered | right-aligned | 

Definition lists
---------------------------

Transcription
: The process by which an RNA molecule is synthesized from a DNA template, resulting in the transfer of genetic information from DNA to RNA.

Translation
: The process by which a sequence of mRNA is converted into a sequence of amino acids, forming a protein during protein synthesis.

---------------------------

Some text with a footnote.[^1]

[^1]: The footnote.

Abbreviations
---------------------------

Markdown converts text to HTML.

*[HTML]: HyperText Markup Language

Emojis
---------------------------

:shipit:
:beaver:

LaTeX math
---------------------------

## Michaelis-Menten Equation
The Michaelis-Menten equation describes the rate of an enzymatic reaction. It is given by:

$$
v = \frac{{V_{\text{{max}}} \cdot [S]}}{{K_{\text{{m}}} + [S]}}
$$

where:
- $v$ represents the reaction rate
- $[S]$ is the substrate concentration
- $V_{\text{{max}}}$ is the maximum reaction rate
- $K_{\text{{m}}}$ is the Michaelis constant

## Needleman-Wunsch algorithm

One famous equation related to bioinformatics is the Needleman-Wunsch algorithm, which is used for sequence alignment. The algorithm calculates the optimal alignment between two sequences based on a scoring system. The equation for the Needleman-Wunsch algorithm is as follows:

$$
F(i, j) = \max \left\{
\begin{array}{ll}
F(i-1, j-1) + S(x_i, y_j) & \text{match/mismatch} \\
F(i-1, j) + g & \text{gap in sequence } x \\
F(i, j-1) + g & \text{gap in sequence } y \\
\end{array}
\right. $$

where:
- $F(i, j)$ represents the score of the alignment at position $(i)$ in sequence $(x)$ and position $(j)$ in sequence $(y)$
- $S(x_i, y_j))$ is the similarity score between characters $(x_i)$ and $(y_j)$ in the sequences
- $(g)$ is the gap penalty
