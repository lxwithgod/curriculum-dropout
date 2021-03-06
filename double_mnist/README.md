## Double MNIST
![Double MNIST Samples](./samples.png)

### The dataset
This is a static version of the [Moving MNIST](http://www.cs.toronto.edu/~nitish/unsupervised_video/) dataset. It is generated by superimposing two random [MNIST](http://yann.lecun.com/exdb/mnist/) digits (either distinct or equal), in order to generate 64x64 images. The total amount of images is 70.000, with 55 classes (10 unique digits classes plus 45 combination of unsorted couples of digits) . Training and test sets contain 60.000 and 10.000 images, respectively. Training set's images are generated  using MNIST training images, and test set's images are generated using MNIST test images. The dataset is stored in the RAM by ``load.py``.

### The code
* The script ``run.sh`` trains the network for 10 different initializations of the weights. Hyperparameters are read from the configuration files in the ``experiments`` folders for each mode (no-, standard-, annealed- and curriculum-dropout). Accuracies are stored in the respective sub-folders.

```
sudo chmod a+x run.sh
./run.sh
```
* The script ``analyseResults_dm_average.py`` plots the average accuracies as a function of the training iterations.
```
python analyseResults_dm_average.py
```
