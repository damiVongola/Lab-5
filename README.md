# Lab-5
This is the fifth Lab for the class Introduction to Machine Learning DIT 45100 AIW01

Install the following python packages needed for this Lab. I would advice that as practice for industry, you install these packages in a virtual environment.

`pip install jupyterlab` `pip install matplotlib` `pip install pandas` `pip install seaborn` `pip install sklearn`

You will be provided with some sample code in sample_code.ipynb that will provide you information that should be enough for you to complete the labs. The following tasks below are our objectives for the lab

You will be implementing the following algorithms we discussed in class:

Clustering with K-means (65 marks)
- Download the california_housing dataset
- Pick just the  "Longitude", "Latitude" and "MedHouseVal" columns of the dataset
- Implement kmeans using sklearn
  - You will be using the default initialization for kmeans namely: "kmeans++"
  - The following will be done in a single for statement
    - You are going to train 6 k-means clustering algorithms with different k's. Specifically k=[5, 6, 7, 8, 9, 10]
    - You will print the following:
       - The plots for each k
       - These will be seaborn scatterplots
       - You will create 6 subplots with shape (2,3) i.e: 2 rows, 3 columns  (The figsize of the plots should be (20, 20))
        - The Latitude will be the y's
        - The Longitude's will be the x's
        - Use random_state=0
        - The MedianHouseValue will serve as the size of each point to let us know which clusters have the houses with the highest value
          - Bigger points will mean bigger MedianHouseValue
      - The inertia for each k (grab these in a list, you will need them later)
      - The Silhoutte score for each k (grab these in a list, you will need them later)
  - Plot the inertia's against k's (y-axis: intertia, x-axis: k)
  - Plot the silhoutte scores against k's (y-axis: silhoutte score, x-axis: k)

Dimensionality reduction with PCA(35 marks)
- We will be using Dimensionality reduction for the purposes of visualization
- Download Breast Cancer dataset from sklearn
- Implement pca using sklearn
  - Perform feature scaling using StandardScaler before applying PCA
  - Print the shape of your scaled data
  - Reduce all features to 2 components
     - Plot a 2D graph with pc1 as x-axis and pc2 as the y-axis
       - Use different points and colors for the "benign" and "malignant" points
     - Print the explained variance ratio
    - Reconstruct back to original dimension
      - Print shape of the reconstructed data
      - Get mse between reconstructed data and scaled data
      Hint: It should be less than 0.4. Around 0.36
  - Reduce all features to 3 components
    - Plot a 3D graph with pc1 as the x-axis, pc2 as the y-axis and pc3 as the z-axis
      - Use different points and colors for the "benign" and "malignant" points
    - Print the explained variance ratio
    - Reconstruct back to original dimension
      - Print shape of the reconstructed data
      - Get mse between reconstructed data and scaled data
      Hint: It should be less than 0.3. Around 0.27

   

