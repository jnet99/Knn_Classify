# Knn_Classify

## Objective
Implement a Python function, knn_classify, to perform k-Nearest Neighbors classification on training data and evaluate it on test data. The function normalizes the data, computes Euclidean distances, and classifies test objects based on the majority vote of the k nearest neighbors.

## Repository Structure
- `data/`: Contains datasets (e.g., `pendigits_training.txt`).
- `gifs/`: Contains GIFs visualizing the classification model's output.

## Code Structure

### `knn_classify_main.py`:
- Sets the dataset directory, dataset name, and hyperparameter (`k`).
- Calls the `knn_classify` function with the specified inputs.

### `knn_classify.py`:
- **Data Loading**: Reads training and test data from UCI-format files.
- **Data Normalization**: Normalizes each dimension using the mean and standard deviation of the training data.
- **Distance Calculation**: Computes Euclidean distances between test objects and training objects.
- **Classification**:
  - Finds the `k` nearest neighbors for each test object.
  - Predicts the class based on majority vote, handling ties randomly.
  - Computes accuracy for each test object.
- **Output**:
  - Prints object ID, predicted class, true class, and accuracy for each test example.
  - Computes and prints the overall classification accuracy.

## Key Features
- Supports configurable `k` values for k-NN.
- Normalizes data to ensure consistent scaling across dimensions.
- Uses Euclidean distance for nearest neighbor calculations.
- Handles ties in predictions by randomly selecting one of the tied classes.

## Testing and Results
- Tested on the `pendigits` dataset with the k being 1,3 and 5.
- Results were consistent with expected performance ranges.

  ![knn_classify_pen_1](https://github.com/user-attachments/assets/1810c6af-83f3-4864-8803-1958d7a8238b)

