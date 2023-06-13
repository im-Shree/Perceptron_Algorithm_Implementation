# Perceptron class
This Perceptron class provides the basic functionalities for training and making predictions with a perceptron model. By using the fit method, you can train the perceptron on a given dataset, and then use the predict method to make predictions on new, unseen data.

### Initialization (__init__ method):
The __init__ method is a special method that initializes the object of the perceptron class. It takes two optional parameters: learning_rate and n_iters. learning_rate (default value: 1) determines the step size for updating the weights during training. n_iters (default value: 100) specifies the number of training iterations. Other attributes of the class include activation_func, weights, and bias, which are initialized as None. These will be set during training.

### Fit (fit method):
The fit method is used to train the perceptron model.
It takes two parameters: X (the input features) and y (the target labels).
It initializes the weights and bias to zeros, and converts the target labels (y) to a binary array (y_) where values greater than 0 are set to 1 and others to 0. The method then iterates n_iters times and for each iteration, it loops through each training example.

For each training example, it computes the linear combination of the input features and weights, adds the bias term, and applies the activation function (_unit_step_func) to get the predicted output.
It calculates the update value based on the difference between the predicted output and the target label, multiplied by the learning rate.
The weights and bias are updated by adding the update value multiplied by the input features and 1, respectively.

### Predict (predict method):
The predict method takes the input features (X) as a parameter and returns the predicted output labels.
It computes the linear combination of the input features and weights, adds the bias term, and applies the activation function to obtain the predicted output.

### Activation Function (_unit_step_func method):
The _unit_step_func method is a private method that serves as the activation function for the perceptron.
It takes a scalar or an array (x) as input and returns 1 where the input is greater than or equal to 0, and 0 otherwise.

### How it performs on Linearly Separable Data
![LS-Data](https://github.com/im-Shree/Perceptron_Algorithm_Implementation/assets/90651908/ba6f55e0-25e2-4fa8-bae5-1f3535d02bb7)

### How it performs on Non-Linearly Separable Data
![NLS-Data](https://github.com/im-Shree/Perceptron_Algorithm_Implementation/assets/90651908/aa86c0db-7dc8-480a-9c2e-26c1f6112a80)
