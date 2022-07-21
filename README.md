# Brain-State-Classification-using-fMRI

How to run the code
 
This work was originally done in Google Colab, so it has a code for loading the data from Google Drive. Therefore, the path of the data files needs to be changed before running the code. The code in the .py file has been changed so that the paths use relative paths. The lines for mounting Google Drive have been commented out.
 
Limitations
 
1. It is difficult to interpret the SVM model
2. It takes a long time to run the model
(as a solution, I ran the code in Colab utilizing their GPU, but I still could not run the function without PCA part on several parameters, so I had to limit my C and gamma values to one or two values)
 
Results

 
The best accuracy overall was 88.43% on ses-test data with (only SVM)
​- 1. threshold=100, 2. C=100, 3. gamma=1e-09
 
For the ses-test data, the accuracy for the model with PCA ranqged from 74% to 88% while for the model without PCA, we had 77% to 88%. For the ses-retest data, the accuracy for the model with PCA ranged from 62% to 77% while for the model without PCA, we had 68% to 71%.
 
When we conduct dimension reduction on the feature vector, it makes it a lot easier for the code to run, but without PCA, it takes a lot longer. As a result, we were only able to test a couple parameters for the C and gamma value (SVM) while we tested more than 10 parameters each for the PCA reduced dataset.
 
Hence, we see a higher accuracy for the ses-retest data with PCA dimension reduction than the model without PCA dimension reduction. If we were able to test more parameters on the model without PCA, we would have gotten a higher accuracy for the model without PCA
