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

## Data analysis (how to use our customised [primer scheme](https://github.com/Kinene1/Grape-Tile-Amplicon-Scheme/tree/main/primer-scheme/Grape/Tile/V2)) 
We recomened using the [InterArtic wrapper](https://github.com/Psy-Fer/interARTIC) created by Ferguson et al 2022 and our primer scheme. Alternatvely one can map raw reads directly to the reference provided in our customised primer scheme using minimap2. 

### Using the InterArtic wrappper. 
The [InterArtic wrapper](https://github.com/Psy-Fer/interARTIC) uses bioinformatics resources from the [ARTIC Network](https://github.com/artic-network/artic-ncov2019) and was originally created to analyse COVID-19 genomes but it is also **suitable for analysis of amplicon schemes like the ones presented here (link)**

### Step 1: 
Install the [InterArtic wrapper](https://github.com/Psy-Fer/interARTIC) and run the test data set provided by Ferguson et al 2022  team. 

### Step 2: 
Initialize InterArtic,  open the interactive web page and select the location of the input data.
- (i) Enter the base file path where your input data is located. 
- (ii) Enter the base file path where your sample-barcode.CSV files are located. Information on how to creat the sample-barcode file can be found [here](https://psy-fer.github.io/interARTIC/usage/#configuring-interartic)
- (iii) Click confirm. 
- (iV) Click add a job.

### Step 3: 
You will now see a page with  tittle **Prepare your InterARTIC job** . Lets put in the required job parameters. 
- (a) Enter a job name, this could be anything related to your experiement /project samples
- (b) Select te input data directory for your experiement, this is the experimental group name that you used on the MinION device. 
- (c) Select multiple samples if you used more than one barcode otherwise single samples
- (d) Enter the name of the output folder, use any name of your choice. Note: if you submited a job and it failed or passed you may need to overide the data or use a different folder name. 
- (e) Enter the primer-scheme top directory. In my case the top directory is Grape, therefore I would enter the path to Grape as: /Kinene1/Grape-Tile-Amplicon-Scheme/tree/main/primer-scheme/Grape. Your path will be different from this depending on the location of the primer-scheme on your local machine. 
- (f) Enter the primer-schme name, in this case use Tile/V2
- (e) Select Already demultiplex with guppy if you did this on the MinION, I recommend doing this on the MinION device. 
- (g) Select the library preparation kit that you used. in this case we used the Rapid library prep kit
- (h) You can set the minimum length and maximum length, Note this will depend on your product size. if your product size is 1500 then your max can be 2000. Otherwise your min should be lower than the smallest product size. 

### Step 4:
- Submit the job. 
- **Note** : for more information on how to set the InterARtic paramters follow the this link https://psy-fer.github.io/interARTIC/usage/




# References 

1.	Ferguson, J. M., Gamaarachchi, H., Nguyen, T., Gollon, A., Tong, S., Aquilina-Reid, C., ... & Deveson, I. W. (2022). InterARTIC: an interactive web application for whole-genome nanopore sequencing analysis of SARS-CoV-2 and other viruses. Bioinformatics, 38(5), 1443-1446.
2.	Quick, J., Grubaugh, N. D., Pullan, S. T., Claro, I. M., Smith, A. D., Gangavarapu, K., ... & Loman, N. J. (2017). Multiplex PCR method for MinION and Illumina sequencing of Zika and other virus genomes directly from clinical samples. Nature protocols, 12(6), 1261-1276.
3.	Tyson, J. R., James, P., Stoddart, D., Sparks, N., Wickenhagen, A., Hall, G., ... & Quick, J. (2020). Improvements to the ARTIC multiplex PCR method for SARS-CoV-2 genome sequencing using nanopore. BioRxiv. doi:https://doi.org/10.1101/2020.09.04.283077
4.	Quick, J. (2020). nCoV-2019 sequencing protocol v3 (LoCost). Protocols. io. https://protocols.io/view/ncov-2019-sequencing-protocol-v3-locost-bh42j8ye
5.	Oxford Nanopore. PCR tiling of SARS-CoV-2 virus. Version PTC_9096_v109_revL_06Feb2020. Downloaded on 11/01/2021


