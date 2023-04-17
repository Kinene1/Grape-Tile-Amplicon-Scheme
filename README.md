# Grape-Tiled-Amplicon-Scheme
Tiled targeted amplicon scheme is a primer scheme for simultaneous detection of 11 grapevine viruses:
The targeted grapevine viruses are litsted as follow.
1. Grapevine Leafroll aaaociated Virus 1 (GLRaV-1)
2. Grapevine Leafroll aaaociated Virus 2 (GLRaV-2)
3. Grapevine Leafroll aaaociated Virus 3 (GLRaV-3)
4. Grapevine Leafroll associated Virus 4 (GLRaV-4)
5. Grapevine Leafroll associated Virus 4 strain 5 (GLRaV-4 strain -5)
6. Grapevine Leafroll associated Virus 4 strain 5 (GLRaV-4 strain -9)
7. Grapevine Virus A (GVA)
8. Grapevine Pinot Gris Virus (GPGV)
9. Grapevine Virus B (GVB)
10. Grapevine Fleck Virus (GFkV)
11. Grapevine Rupestris Stem Pitting assocciated Virus (GRSPaV)

Our customised [primer scheme](https://github.com/Kinene1/Grape-Tile-Amplicon-Scheme/tree/main/primer-scheme/Grape/Tile/V2) is to used with the **targted amplicon sequencing assay for simultaneous detection of eleven grapevine viruses assay** link..

## Data analysis (how to use our customised primer scheme) 
We recomened using the [InterArtic wrapper](https://github.com/Psy-Fer/interARTIC) created by Ferguson et al 2022 and our primer scheme. Alternatvely one can map raw reads directly to the reference provided in our customised primer scheme using minimap2. 

### Using the InterArtic wrappper. 
The [InterArtic wrapper](https://github.com/Psy-Fer/interARTIC) uses bioinformatics resources from the [ARTIC Network](https://github.com/artic-network/artic-ncov2019) and was originally created to analyse CoV-2 but it is also ** suitable for analysis of amplicon scheme like the ones presented here (link)

### Step 1: 
Install the [InterArtic wrapper](https://github.com/Psy-Fer/interARTIC) and run the test data set provided by Ferguson et al 2022  team. 

### Step 2: 
Initial InterArtic,  open the interactive web page and select the location of the input data.
(i). Enter the base file path where your input data is located. 
(ii). Enter the base file path where your sample-barcode CSV files are located. 
(iii). Click confirm. 
(iV). click add a job.

### Step 3: 
You will now see a page tittle with **Prepare your InterARTIC job** . Let put in the required job parameters. 
(a). Enter a job name, this could be anything related to your experiement /project samples
(b). Select te input data directory for your experiement, this is the experimental group name that you used on the MinION device. 
(c). select multiple samples if you used more than one barcode otherwise single samples
(d). Enter the name of the output folder, use any name of your choice. Note if you have submited a job and it failed or passed you may need to overide the data or use a different folder name. 
(e). Enter the primer scheme top directory. In my case the top directory is Grape, therefore I will enter the path to Grape as: /Kinene1/Grape-Tile-Amplicon-Scheme/tree/main/primer-scheme/Grape. Your path will be different from this depending on the local of the primer-scheme on your local machine. 
(f). Enter the primer schme name, in this case use Tile/V2
(e). Select Already demultiplex with guppy if you did this on the MinION, I recommend doing this on the MinION device. 
(g). Select the library preparation kit that you used. in this case we used the Rapid library prep kit
(h). You can set the minimum length and maximum length, Note this will depend on your product size. if your product size is 1500 then your max can be 2000. Otherwise your min should be lower than the smallest product size. 

### Step 4:
Submit the job. 
**Note** for more information on how to set the InterARtic paramters follow the this link https://psy-fer.github.io/interARTIC/usage/




