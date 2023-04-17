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

## Step 3: 
You will now see a page tittle with **Prepare your InterARTIC job** . Let put in the required job parameters. 
(a). 



