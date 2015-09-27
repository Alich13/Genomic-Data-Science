# [Genomic Data Science Specialization (Johns Hopkins University and Coursera)] (https://www.coursera.org/specialization/genomics/41)


### Incentives & Benefits
High-throughput experimental techniques have enabled the Data Science revolution in modern biology. People with skills in biology, computations and statistics are fundamental to this change. This Specialization will help you be a part of the new wave of Big Data Science in Genomics. These skills are in high demand across modern biology, from bench scientists in industry and academia to data scientists working with healthcare analytics.

### Courses
This specialization will teach you to understand, analyze, and interpret data from next-generation sequencing experiments. You will learn common tools of genomic data science, including Python, R, Bioconductor, and Galaxy. These courses can serve as a stand-alone introduction to genomic data science or can compliment to a primary degree or postdoc in biology, molecular biology, or genetics. The Specialization concludes with a Capstone project that allows you to apply the skills you've learned throughout the courses.

### Projects

#### Project1 -- Concepts of Genomic Data Science

In this project you will be reading a genomic data science paper and answering some questions to help you learn about how the different fields in genomic data science work together and to evaluate your understanding of some of the concepts we have learned throughout the course. The paper we are reading is called: “Microbial Genes in the Human Genome: Lateral Transfer or Gene Loss?” You can access the paper from the Science Magazine site here: http://www.sciencemag.org/content/292/5523/1903.full.

[Project Solution](https://github.com/lanttern/Genomic-Data-Science/blob/master/Course1_Introduction%20to%20Genomic%20Technologies/Course%20Project_test2.pdf)

#### Project2 -- Identify DNA Polymorphic Sites with Galaxy

[Published Page]( https://usegalaxy.org/u/coursera/p/genomic-data-science-with-galaxyidentify-polymorphic-sites)

This page includes description about analyses of DNA polymorphic sites of father-mother-child sequencing samples:

Stage 1 - identify polymorphic sites

step 1: load data - the data are loaded from local files, set "fastqsanger" format and "hg19" database on the starting page

step 2: check quality of all sequencing files - use FastQC tool (version: 0.63) to check quality of the sequencing

step 3: mapping - use BWA-MEM tool (version: 0.1) to map sequence to reference genome (choose hg19 as reference), paired end

step 4: add or replace read groups - label each group (the mapping file) using AddOrReplaceReadGroup (version: 1.126.0)

step 5: merge 3 individual mapping files - use MergeSamFiles (version: 1.126.0)

step 6: filter - using filter tools: Filter (version: 1.126.0, remove low quality mapping), MarkDuplicates (version: 1.126.0, filter out duplicated mapping), CleanSam (version: 1.126.0)

step 7: identify polymorphic sites - using FreeBayes tool (version: 0.4) to identify polymorphic sites base on hg19 genome

step 8: filter out false positive sites - using VCFfilter (version: 0.0.3) to select sites where the chance of a false positive call is 1 in 10,000 or better.

step 9: extract workflow and download final vcf file for further analyses.

Stage 2 - analyze data of polymorphic sites based on vcf file

step 10: load data - set format as "vcf", genomic database as hg19

step 11: identify number of snp, mnp, del, ins or complex - using VCFfilter tool (version:0.0.3 ) to select different types of polymorphism (for example: -f "TYPE = snp", select snp only), then using Filter tool (version: 1.1.0) to find duplicated polymorphisms

step 12: identify genes with polymorphic sites - using ANNOVAR Annotate VCF tool (version: 0.1) to annotate the  vcf file in step 10

step 13: count polymorphic sites for each gene - using Group tool (version: 2.1.0, by gene name) to count number of polymorphic sites for each gene

step 14: sort results in step 13 using Sort tool (version: 1.0.3, by descending).

[WorkFlow](https://usegalaxy.org/workflow/display_by_username_and_slug?username=coursera&slug=workflow-constructed-from-history-genomic-data-science-with-galaxy-project---completed)

[History for Analyses](https://usegalaxy.org/u/coursera/h/workflow-constructed-from-history-genomic-data-science-with-galaxy-project---completed)
