## What is overfitting?
Overfitting occurs when a machine learning model learns the training data too well, capturing not only the underlying patterns but also the noise and random fluctuations specific to the training dataset. An overfitted model performs exceptionally well on training data but fails to generalize to new, unseen data. This happens because the model has essentially "memorized" the training examples rather than learning generalizable patterns.
## How do you determine your model is overfitting?
#### Before concluding overfitting, rule out:
- Loss is high on training data as well:
  - Model bias: Ensure the model type is capable of representing the underlying pattern
  - Insufficient optimization: Verify the model has been properly trained
- Train-test distribution mismatch: Confirm that test data comes from the same distribution as training data, as distributional shifts can mimic overfitting symptoms
#### Several indicators suggest your model may be overfitting:
- Performance gap: Loss is low on training data but high on testing data. This divergence in performance is the most classic sign of overfitting.
- Learning curves analysis: When plotting training and validation error over time/epochs, an overfitted model shows continually decreasing training error while validation error begins to increase after a certain point.
- Complex decision boundaries: Visualizations of decision boundaries that appear overly complex or convoluted to capture every training point precisely.
- Sensitivity to small data changes: Overfitted models often show high variance, with small changes in training data causing large changes in predictions.

## Ways to mitigate overfitting

#### Data-focused approaches:

- Collect more data: More diverse training examples help the model learn generalizable patterns instead of memorizing specific instances.
- Data augmentation: Create synthetic variations of existing data through transformations (rotation, scaling, noise addition) to increase effective training set size.
- Feature selection: Remove irrelevant or redundant features that might lead to spurious correlations.

#### Model complexity reduction:

- Simplify model architecture: Use fewer parameters, features, or layers to limit model capacity.
- Pruning: Remove unnecessary connections or units in neural networks after initial training.
- Dimensionality reduction: Apply techniques like PCA to reduce input dimensionality.

#### Regularization techniques:

- L1/L2 regularization: Add penalty terms to the loss function that discourage **large weights**.
- Dropout: Randomly disable neurons during training to prevent co-adaptation and create an ensemble effect.

#### Training process modifications

- Early stopping: Halt training when **validation performance begins to degrade**.

#### Validation strategies

- K-fold cross-validation: Divide data into k subsets, training k different models each using a different subset as validation data, then average results.

