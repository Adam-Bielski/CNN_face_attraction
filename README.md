# CNN for faces classification
### Classification of faces based on their attractiveness + checking for correlation between attractiveness and the number of subscription on youtube

------------------------------------------
#### Quick Summary

*The aim of the project is to predict attractiveness of the biggest 300 youtubers on learned CNN and check if there's a statistically valid correlation between their assessed attractiveness and the number of subscribers they have. It's been long speculated that being attractive can boost one's chances of being successful on youtube. This projects can confirm and disprove this thesis with high accuracy.

#### Steps taken in the projects

The steps to achieve it are as following:*

   
   1. *Train an auxilliary CNN to detect and rate such face features as: hair, facial hair, eyes, nose, cheeks, lips, age, gender, on images*
   2. *Train the final CCN to asses attractiveness based on those features and alongside with image contents*
   3. *Web-scrape the names of 300 most popular youtubers*
   4. *Save 10 top images that pop up after writing name of those youtubers in Google Image*
   5. *Based on 10 images per youtubers assess their attractivess*
   6. *Run statistical analysis to check if there's a statistically valid correlation*
   
   
#### Source of data (face images)

Face images used to train models were collected by researchers at MMLAB, The Chinese University of Hong Kong.
Their website can be found under the link: http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html
As mentioned on the website, the CelebA dataset is available for non-commercial research purposes only. For specifics please refer to the website.

The algorithm relies on the correct specification of the data when it comes to the assessed attractiveness and other characteristics

   
   
   




