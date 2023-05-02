Since the code is written in a notebook, all instructions and the outputs are displayed.


Question 1

To manipulate the images, PIL library from Python is used.
When reading the image files, to find the index of the given image, a simple if statement
is used:

"if imgPath == "/content/afhq_dog/flickr_dog_000002.jpg": ......"

(Normally, the given image is the first image in the dataset but maybe it is because the way 
that I read the images, they all shuffled.)

I defined a function called PCA() which inputs the dataset and outputs the eigenvalues
and eigenvectors

To find the eigenvalues and eigenvectors, I used np.linalg.eig from NumPy as stated in the
homework document.

Another function is PVE() which inputs eigenvalues and outputs the PVE values.

The function principal() inputs eigenvectors and the k values and outputs the
first k principal components.

To ease the process of reshaping, I wrote the function reshaping()which inputs the
channel input, the number of images, and the requested sizes, and outputs the reshaped
array.

I followed the instructions and displayed the images as seen in the notebook file.


Question 2

First of all, I shuffled the dataset and split them into training, validation and test 
datasets in the given proportions.

Then I defined a function called TrainAndTest() which inputs batch_size, weights, bias,
training_set, validation_set, training_label, validation_label, and learning rate. It
outputs epoch accuracies and predicted labels.

Inside TrainAndTest() I implemented gradient ascent algorithm along with the logistic
regression algorithm.

Using this function I tried all the candidates for hyperparameters and found the optimal ones.
