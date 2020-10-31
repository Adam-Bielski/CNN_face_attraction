# CNN for faces classification
### Classification of faces based on their attractiveness + checking for correlation between attractiveness and the number of subscription on youtube
<br/><br/>
<br/><br/>
<br/><br/>
------------------------------------------
#### Quick Summary

*The aim of the project is to predict attractiveness of the biggest 300 youtubers on learned CNN and check if there's a statistically valid correlation between their assessed attractiveness and the number of subscribers they have. It's been long speculated that being attractive can boost one's chances of being successful on youtube. This projects can confirm and disprove this thesis with high accuracy.*
<br/><br/>
#### Steps taken in the projects

*The steps to achieve it are as following:*

   
   1. *Train an auxilliary CNN to detect and rate such face features as: hair, facial hair, eyes, nose, cheeks, lips, age, gender, on images*
   2. *Train the final CCN to asses attractiveness based on those features and alongside with image contents*
   3. *Web-scrape the names of 300 most popular youtubers*
   4. *Save 10 top images that pop up after writing name of those youtubers in Google Image*
   5. *Based on 10 images per youtubers assess their attractivess*
   6. *Run statistical analysis to check if there's a statistically valid correlation between attractiveness and the number of subscribers*
   
<br/><br/>
#### Source of data (face images)

Face images used to train models were collected by researchers at MMLAB, The Chinese University of Hong Kong.
Their website can be found under the link: http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html
As mentioned on the website, the CelebA dataset is available for non-commercial research purposes only. For specifics please refer to the website.

The algorithm relies on the correct specification of the data when it comes to the assessed attractiveness and other characteristics

<br/><br/>

-----------------------------------
   
#### Preprocessing of images


Each image has to undergo a preprocessing, which include:


   1. Pruning of images
         * Detecting a face
         * Getting coordinates of the box around a face 
         * Cutting off image to fit the 150% size of the box
         
         Although raw images are already faces, performance of the classifier will be higher if we cut off unnecessary stuff. 150% of the size of boxes ensures that    hair/eyeglasses/facial hair will be included on an image.
         
   2. Padding of images
         * Padding images with monochromatic borders so that they have the same dimensions
         * If an image doesn't fit (is larger) than the target dimensions or the detected face is extremely small, then an image is discarded
         
         Arguably CNN will work better with images of common size.
         
         
Example of such preprocessing:


![alt text](https://github.com/Adam-Bielski/CNN_face_attraction/blob/main/Figures/Preprocessing%20image.jpg)


<br/><br/>


#### Building CNNs


   1. Build auxiliary CCNs to detect face features, such as:
         * Eyeglasses
         * Hair (Bald, Receding hairline)
         * Facial hair (Mustache, Beard, Sideburns, 5_o_clock_shadow, Goatee, Double Chine)
         * Eyes (Narrow eyes, Bags under eyes)
         * Cheeks (Rosy cheeks, High cheeks)
         * Lips (Big lips)
         * Young
         * Gender
  
  
  Some features are used to predict others. To get better understanding of it, look at the graph below:       
         
 ![alt text](https://github.com/Adam-Bielski/CNN_face_attraction/blob/main/Figures/Flow_jpg.jpg)
 
 
 2. Build final CNN to predict attractiveness of a face
 
 
 
 
 
 
 



  
   
 




