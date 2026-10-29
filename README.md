# IGV Genome Brower Tracks with ENCODE Data
## IGV Genome Brower
IGV [1-4] can be used as a web app or a desktop application, and offers a simple method to explore ENCODE data and other genomic datasets. For this tutorial, we will show the web app specifically, but a similar process can be used with the desktop app. We'll also show an example JSON file that can be loaded into IGV. First navigate to https://igv.org/app/.  

## Loading tracks from ENCODE
To load a single track go to Tracks > URL …  

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/5e4c6c60-d979-4e6f-a8c8-67835f7591be" />  
</div>  

This will pull up a place to enter URLs to pull tracks:  

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/04db7283-4f57-4c62-83a0-882507c8241b" />  
</div>  

You can identify ENCODE datasets to plot either by navigating the data portal or searching for known datasets. For example, if we wanted to load ENCODE-rE2G predictions for left colon from Donor ENCDO856ZOJ like we did in the example figure in the paper we could search ten ENCODE portal with something like “ENCODE-rE2G predictions colon Donor ENCDO856ZOJ,” which brings up the following results:  

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/cf2697e0-c83d-48d3-8bb0-f67c65141fe7" />  
</div>  

Click on Annotation file set: ENCODE-rE2G predictions for left colon; Donor: ENCDO856ZOJ, which brings up this page:  

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/6fb38802-0767-4814-b7c4-eb43c24b05e1" />
</div>  

Then click on File Details to view the different associated files:

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/e30c8fc2-336e-4c64-aeab-db428794682a" />
</div>  

In this case we will plot the bedpe threshold links. Right click on the blue download icon and copy the link:

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/23e9df12-6cbb-4c3b-bd68-c7da5484c4b7" />
</div>  

Now go back to IGV and paste this link into Track URL and click OK.  

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/ea8b2e53-b7d8-44c7-a447-f0b09216d910" />
</div>  

This will load the file into your browser session. Now paste a region of interest in IGV and press enter. For example, chr11:2,188,204-2,320,124 contains the region around ASCL2 so we can go to that region here. Now we see predicted E2G links around ASCL2:  

<div style="text-align: center;">
  <img width="468" height="178" alt="image" src="https://github.com/user-attachments/assets/20cfc843-2144-4d2e-b0c8-6c20888ffaea" />
</div>  

Click the gear to the right of the track to edit visual properties such as track height, track color, name, or direction. Here we change the name to “59F Threshold E2G Predictions (bedpe),” the height to 100, and the color to dark blue.  

Lets say you now wanted to add DNase data from the same donor. Navigate the DNase-seq experimental data page for that patient:  

<div style="text-align: center;">
  <img width="468" height="247" alt="image" src="https://github.com/user-attachments/assets/a2ba09f3-38c9-45c1-bd0d-f5bd7887067f" />
</div>  

Again click on file details and copy the link to the read-depth normalized bigwig file:  

<div style="text-align: center;">
  <img width="468" height="308" alt="image" src="https://github.com/user-attachments/assets/34b73de5-be2e-4843-bb9f-462df4f76aa2" />
</div>  

Go back to IGV and again go to Tracks > URL… and past in the URL.  

<div style="text-align: center;">
  <img width="468" height="138" alt="image" src="https://github.com/user-attachments/assets/7f9a8146-d8d3-46ac-886c-e170bb5db6e6" />
</div>  

Now the DNase track should also be visible. 

<div style="text-align: center;">
  <img width="468" height="235" alt="image" src="https://github.com/user-attachments/assets/80aed55a-26ae-4788-95a2-d55b451cbf02" />
</div>  

Similar to before, you can click on the gear to the right to change properties such as colors, height, name, and scale of the track. 


## Loading custom data
The user can also load tracks that they have defined from custom datasets to plot alongside the ENCODE data. While there are some pseudobulks available on the ENCODE portal, for the figure we defined pseudobulks for each cell type in ArchR, just using the two colon multiome datasets. For custom data such as this, the user can upload the data to locations such as dropbox or google drive to load into the genome browser. As an example, I uploaded the data to dropbox and made the links public. In this case, you can use the same Tracks > Add URL process to add the genomic tracks. 

<div style="text-align: center;">
  <img width="468" height="136" alt="image" src="https://github.com/user-attachments/assets/948fbd3a-31dd-4796-9f48-29c253ed27ce" />
</div>  

Clicking okay will load the track that you uploaded to dropbox. 

<div style="text-align: center;">
  <img width="468" height="221" alt="image" src="https://github.com/user-attachments/assets/134e2cab-f089-4235-8747-97029171ef10" />
</div>  

## Saving IGV Session JSON Files:

It is good practice to save a browser session as a JSON file if you might go back to it later. To do this, go to the top and click Session and Save...  

<div style="text-align: center;">
  <img width="468" height="171" alt="image" src="https://github.com/user-attachments/assets/19827039-ec10-4524-9510-4ff935a7a799" />
</div>  

Give it a name and the click okay to download a JSON file of the session.

<div style="text-align: center;">
  <img width="468" height="141" alt="image" src="https://github.com/user-attachments/assets/65316043-0932-4268-87b3-fec0ed9d1bd4" />
</div>  

The session can then be reloaded in the future by going to Session and Local File… and selection the JSON file. 

<div style="text-align: center;">
  <img width="468" height="175" alt="image" src="https://github.com/user-attachments/assets/c39032d0-71f1-4fef-8a72-f3a7437d96bf" />
</div>  

## Editing IGV JSON Files:
It can also be helpful to edit a JSON file directly, especially if you are making multiple tracks and changing a lot of the features. The format of the JSON file includes many basic fields specifying the genome as well as a "tracks" section where you can add additional tracks and specify plotting features for each track such as color, height, orientation, and order.  
 
```
{
	"version": "2.15.13",
	"showSampleNames": false,
	"reference": {
		"id": "hg38",
		"name": "Human (GRCh38/hg38)",
		"fastaURL": "https://igv-genepattern-org.s3.amazonaws.com/genomes/seq/hg38/hg38.fa",
		"indexURL": "https://igv-genepattern-org.s3.amazonaws.com/genomes/seq/hg38/hg38.fa.fai",
		"cytobandURL": "https://s3.amazonaws.com/igv.org.genomes/hg38/annotations/cytoBandIdeo.txt.gz",
		"aliasURL": "https://s3.amazonaws.com/igv.org.genomes/hg38/hg38_alias.tab",
		"chromosomeOrder": "chr1, chr2, chr3, chr4, chr5, chr6, chr7, chr8, chr9, chr10, chr11, chr12, chr13, chr14, chr15, chr16, chr17, chr18, chr19, chr20, chr21, chr22, chrX, chrY"
	},
	"locus": "chr11:2,188,204-2,320,124",
	"roi": [],
	"tracks": [
		{
			"type": "sequence",
			"order": -9007199254740991
		},
		{
			"url": "https://www.dropbox.com/scl/fi/k7pcvligxpnccqa4fqn2y/encode_e2g_predictions_left_colon_ENCSR867XFA_thresholded_predictions.bedpe.gz?rlkey=jgll7rqi3jumodbvol77j8qti&st=8jmc3u9m&dl=0",
			"url": "https://www.encodeproject.org/files/ENCFF577BJW/@@download/ENCFF577BJW.bedpe.gz",
			"name": "59F Threshold E2G Predictions (bedpe)",
			"format": "bedpe",
			"type": "interact",
			"height": 100,
			"order": 1,
			"color": "#004a88",
			"arcOrientation": false
		}
	]
}
```

You can add additional tracks to the JSON file as follows:  

```
		{
			"url": "https://www.encodeproject.org/files/ENCFF755FPE/@@download/ENCFF755FPE.bigWig",
			"filename": "ENCFF755FPE.bigWig",
			"name": "61F DNase",
			"format": "bigwig",
			"type": "wig",
			"color": "#90AFC5",
			"order": 4
		},
		{
			"url": "https://www.encodeproject.org/files/ENCFF718FVY/@@download/ENCFF718FVY.bigWig",
			"filename": "ENCFF718FVY.bigWig",
			"name": "41F H3K27Ac",
			"format": "bigwig",
			"type": "wig",
			"color": "#2A3132",
			"order": 5
		},
		{
			"url": "https://www.encodeproject.org/files/ENCFF163IDS/@@download/ENCFF163IDS.bigWig",
			"filename": "ENCFF163IDS.bigWig",
			"name": "61F_ATAC",
			"format": "bigwig",
			"type": "wig",
			"color": "#763626",
			"order": 6
		}
```



## References
[1] James T. Robinson, Helga Thorvaldsdóttir, Wendy Winckler, Mitchell Guttman, Eric S. Lander, Gad Getz, Jill P. Mesirov. Integrative Genomics Viewer. Nature Biotechnology 29, 24–26 (2011).

[2] Helga Thorvaldsdóttir, James T. Robinson, Jill P. Mesirov. Integrative Genomics Viewer (IGV): high-performance genomics data visualization and exploration. Briefings in Bioinformatics 14, 178-192 (2013).

[3] James T. Robinson, Helga Thorvaldsdóttir, Aaron M. Wenger, Ahmet Zehir, Jill P. Mesirov. Variant Review with the Integrative Genomics Viewer (IGV). Cancer Research 77(21) 31-34 (2017).

[4] James T. Robinson, Helga Thorvaldsdóttir, Douglass Turner, Jill P. Mesirov. igv.js: an embeddable JavaScript implementation of the Integrative Genomics Viewer (IGV). Bioinformatics, 39(1) (2023), btac830.
