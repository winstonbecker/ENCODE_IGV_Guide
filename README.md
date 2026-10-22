# IGV Genome Brower Tracks with ENCODE Data
## IGV Genome Brower
IGV [1-4] can be used as a web app or a desktop application, and offers a simple method to explore ENCODE data and other genomic datasets. For this tutorial, we will show the web app specifically, but a similar process can be used with the desktop app. First navigate to https://igv.org/app/.  

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

<div style="text-align: center;">
  <img width="80%" alt="image" src="https://github.com/user-attachments/assets/a76c9b3d-d88e-4a56-9e19-82a019881b35" />
</div>  






## References
[1] James T. Robinson, Helga Thorvaldsdóttir, Wendy Winckler, Mitchell Guttman, Eric S. Lander, Gad Getz, Jill P. Mesirov. Integrative Genomics Viewer. Nature Biotechnology 29, 24–26 (2011).

[2] Helga Thorvaldsdóttir, James T. Robinson, Jill P. Mesirov. Integrative Genomics Viewer (IGV): high-performance genomics data visualization and exploration. Briefings in Bioinformatics 14, 178-192 (2013).

[3] James T. Robinson, Helga Thorvaldsdóttir, Aaron M. Wenger, Ahmet Zehir, Jill P. Mesirov. Variant Review with the Integrative Genomics Viewer (IGV). Cancer Research 77(21) 31-34 (2017).

[4] James T. Robinson, Helga Thorvaldsdóttir, Douglass Turner, Jill P. Mesirov. igv.js: an embeddable JavaScript implementation of the Integrative Genomics Viewer (IGV). Bioinformatics, 39(1) (2023), btac830.
