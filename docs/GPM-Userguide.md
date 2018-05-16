# ![Pangu](images/logo.png) [LIMS Docs](README.md)
## [GPM Manual](GPM-Manual.md) > Genome Puzzle Master Basic User Guide
- [GPM Workflow](#gpm-workflow)
- [GPM Main Interface](#gpm-main-interface)
- [Uploading A New Genome](#uploading-a-new-genome)
- [Running Preliminary Alignments](#running-preliminary-alignments)
- [Creating a Project and Assigning Genomes](#creating-a-project-and-assigning-genomes)
- [Creating an Assembly](#creating-an-assembly)
- [Running an Assembly](#running-an-assembly)
- [Chromosome View](#chromosome-view)
- [“Cleaning Up” and Moving Contigs](#cleaning-up-and-moving-contigs)

### GPM Workflow
- Upload Subject and Reference Genomes.
- Run preliminary alignments of each subject Genome to the Reference.
- Run an assembly of each Genome.
- “Clean Up” each Chromosome for the assemblies.
- Fill any possible gaps using alternative assemblies of the same subject.  
- Eliminate any identifiable contamination.  

### GPM Main Interface
> The “General” tab is used to upload and manage genomes.
> The “Assembly” tab is used to create assemblies of contigs and align them to chromosomes.  
> ![GPM Main Interface](images/GPM_Screenshots/Slide1.PNG)

### Uploading A New Genome
From the GPM main page, click on the "General" tab on the top toolbar.   
1. Click on "Genomes > New Genome"  and fill out the “Genome Name” field.  
2. Browse for the selected fasta file or copy and paste the file path into the box.  
3. Check the box allowing the genome to be reassembled using Genome Puzzle Master. (If the genome is to be assigned as a reference, check the “Enable as reference" box.)
4. Specify any descriptive information about the genome being uploaded (ex. File path,estimated size, etc.).
5. Click the save button.
![Uploading A New Genome](images/GPM_Screenshots/Slide2.PNG)

### Running Preliminary Alignments
1. From the General Tab, on the GPM main screen, click "Run Alignment".
2. Select the uploaded Query genome from the dropdown menu.
3. Select the uploaded Reference of Subject Genome.
4. Specify the Minimum Overlap and Minimum Identity parameters.
5. Click "Run Alignment" to begin the alignment process.  (The alignment process may take several hours and uses a lot of computational resources). 
![Running Preliminary Alignments](images/GPM_Screenshots/Slide3.PNG)

### Creating a Project and Assigning Genomes
1. Click on the "Assembly" tab from the GPM toolbar.
2. Create a new GPM project by clicking on the "New GPM Project" tab.  This is where all of the genomes for the specified project will be assigned for easy organization.
3. Name the GPM project and add a description if necessary.
4. Check the boxes of all of the genomes to be assigned to this project.
5. Click Save when finished.
6. The selected genomes will now be listed under the created project.
![Creating a Project and Assigning Genomes](images/GPM_Screenshots/Slide4.PNG)

### Creating an Assembly
1. Select the genome to be assembled from the project on the left hand side of the screen.  
2. First, a reference genome must be assigned by clicking the "Assembly Tools" Button.
3. Select the desired uploaded reference genome from the dropdown menu.  
4. Assign “Gap Filler” genomes by checking boxes in the “Extra Genomes” field. 
5. Click “Save” when finished.
![Creating an Assembly](images/GPM_Screenshots/Slide5.PNG)

### Running an Assembly
1. click on the “Assembly Tools” button and select “Run Assembly”. 
2. Specify the desired assembly parameters (ensure the correct reference genome is being used.)
3. Click “Run Assembly”.
![Running an Assembly](images/GPM_Screenshots/Slide6.PNG)

- Before: all contigs are unplaced. 
![all contigs are unplaced](images/GPM_Screenshots/Slide7.PNG)

- After: contigs are numbered and assigned to chromosomes.  
![contigs are numbered and assigned](images/GPM_Screenshots/Slide9.PNG)

### Chromosome View
To view the entire chromosome and all of its assigned contigs, click on the Chromosome number. 
![Chromosome View Click](images/GPM_Screenshots/Slide11_2.PNG)
> ![Chromosome View](images/GPM_Screenshots/slide11_1.PNG)

To view two assemblies side-by-side for easy visualization and facilitated gap filling, select a companion assembly from the drop down menu in chromosome view.
![Companion Chromosome View Click](images/GPM_Screenshots/sLIDE12_1.PNG)
> It will appear on top of the target assembly.
> Note that not all of the contigs will be perfectly aligned with their start and end points on the reference genome and will have to be moved.
> ![Companion Chromosome View](images/GPM_Screenshots/Slide12_2.PNG)

### “Cleaning Up” and Moving Contigs
Here is an example of what it looks like when a contig needs to be moved.  

It can be seen that the alignment (red and yellow lines) of example contig (top blue line) begins much earlier in the reference genome (middle green line)  than where it is currently placed.  

The general idea is to determine where the alignment begins by following the path of red and yellow lines to where it intersects with the reference genome, and then move the contig to that point.  
![Cleaning Up and Moving Contigs](images/GPM_Screenshots/Slide13.PNG)

* Moving Contigs
> By scrolling to the left we can determine where that point of origin is. 
![Moving Contigs](images/GPM_Screenshots/Slide14_2.PNG)

> From here, scroll back to the contig to be moved, right click on the blue portion, and click edit contig.  
![Edit Contig](images/GPM_Screenshots/Slide14_1.PNG)

> In this example, the alignment point of origin was approximately 40,150,000 bp.  We will change the “Estimated Position” field to this value.  
![Edit Contig Pisition](images/GPM_Screenshots/Slide15_2.PNG)

> Shown is the new placement at 40,150,000bp. It clearly aligns well with its counterpart contig from the companion assembly.  
![Edit Contig After](images/GPM_Screenshots/slide16.PNG)
