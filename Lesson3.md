# Deep Learning
## Lesson 3


<h3>What is a Cost function?</h3> Cost Function ia a method of evaluating how well a machine learning algorithm predicts the output by comparing the predicted target lables with the known target labels. If predictions are pretty good, loss function will have a lower value. If not,the loss function will have a high value.

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160310814-f3f65cd5-a0ef-472e-8653-b749bed0b296.PNG" width="550" title="hover text">
</p>

* <strong>Multi-class SVM loss</strong> Multi-class SVM Loss is a cost or a loss function that uses a scoring function 'f' to determine the numerical scores for each target class labels. 
<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160311593-3c45d078-7f8c-4453-a3bf-3d8ff3d29625.PNG" width="350" title="hover text">
</p>


For the cat prediction ,loss would be calculated as shown in the figure below

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160311623-39c65485-24be-4187-9a70-8ba185f21485.PNG" width="450" title="hover text">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160311869-e53a6fbf-1e08-4316-9a6b-b2e529784136.PNG" width="450" title="hover text">
</p>

<h3>Regularization</h3> Regularization is a process that is used to minimize the loss function and prevent overfitting or underfitting.

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160312380-369df648-c3d9-4857-93ef-7bbff080ba38.PNG" width="550" title="hover text">
</p>

<h3>Types of Regularization</h3>

* <strong>L1 Regularization</strong> In L1 regularization(also known as Lassso Regression), a regularization term equal to the absolute value of magnitude of coefficient is added to the cost function as penalty term. L1 regularization can be used for feature selection.

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160312859-1c68b7d2-a850-4896-b690-ac2f8d55728b.PNG" width="450" title="hover text">
</p>

* <strong>L2 Regularization</strong> In L2 regularization(also known as Ridge Regression), a regularization term equal to the square value of magnitude of coefficient is added to the cost function as penalty term. If we have features which are highly correlated top each other, we can use the L2 regularization as it allows the less signinficant features to have some influence at predicting the outcome rather than eliminating it all together.

<p align="center">
  <img src="https://user-images.githubusercontent.com/45029614/160313579-2bf66030-904a-43c9-b32f-85000c32dd72.PNG" width="450" title="hover text">
</p>

<strong> Elastic Net Regularization</strong> Elastic Net Regularization is the combination of Lasso and Ridge regression.

