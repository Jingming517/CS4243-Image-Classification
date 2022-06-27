# CS4243-Image-Classification

## Project Aim
- We aim to classify whether an image is Computer Generated Imagery (CGI) or Photographic Image (PI)
- CGI: still or animated content made with computer software and is typically used in movies, television and games
- PI: a picture made using a camera

## Project Motivation
- Advances in CGI software and AI are creating increasingly realistic images
- In an experiment on 200 participants, they could only differentiate AI generated images from real images 48.2% of the time.
- We have decided to focus our project on images of human faces because we believe that this is where the greatest potential for abuse lies
  <img width="485" alt="image" src="https://user-images.githubusercontent.com/53804726/175858128-57698368-6105-4fe8-a83c-5c209697a506.png">

## Related works
- Wu et al., used histograms of the difference images (i.e. the images composed of differences of adjacent pixels) and afterwards takes the most informative histograms as features. 
  <img width="198" alt="image" src="https://user-images.githubusercontent.com/53804726/175858213-f1634780-4f32-48a1-b704-a65cc99d1687.png">

- Rahmouni et al. uses histograms to a CNN framework and finds the best features for efficient boundary
- Nguyen et al. proposes the use of a modular VGG-19 as the main model 
- For our project, we would like to explore the VGG model and find out the internal workings of the multiple layers. We would also like to explore our dataset and decide on our own features to include as inputs to the model (see section 3 and 4 for said features).

## Data collection
- We created our own scraper to scrape Google Images
- Made use of Selenium and Requests libraries
  <img width="229" alt="image" src="https://user-images.githubusercontent.com/53804726/175858326-e3925c08-8847-487a-9fb7-40fbdd974d81.png">
- Using just "CGI faces" and "photos of faces" as search queries would have been too broad and resulted in a lot of noise in the dataset.
- We had to find a way to segment the search queries
- Segment the "CGI" dataset using the different use cases of CGI images - games, movies and television shows. 
- Segment the photographic images based on ethnicity so as to gather a diverse dataset. 
- Some of the search results resulted in duplicated images - use difPy library to remove them
- Total of ~7000 images collected


## Data exploration
- Edge detection
- Image resolution
- Cropping vs resizing vs black borders

## Preprocessing
1. Center crop all the photos we had into 128 * 128 dimensions, in RGB.
2. Apply gray scale
3. Blur the grayscale image
4. Use (3) for sobelx, sobely, sobelxy edge detection
5. Use (3) for canny edge detection
6. Combine R,G,B,sobelx, sobely, sobelxy, canny edge detection data as inputs
7. Split into respective training and test set to be passed into the models.

## Data analysis with deep learning
### 1. Logistic Regression
- benchmark for all the other more complex CNN models
- one single linear layer
  <img width="1046" alt="image" src="https://user-images.githubusercontent.com/53804726/175858668-79b228f7-047a-403d-a151-75056bf0d2d5.png">

## 2. AlexNet
- five convolutional layers + three fully-connected layers.
- Overfitting problem
  <img width="1016" alt="image" src="https://user-images.githubusercontent.com/53804726/175858768-040467bb-f2d5-4c4b-9f70-5ace0373599f.png">


























