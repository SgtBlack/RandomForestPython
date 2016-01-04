# RandomForestPython

# decision-tree
A C4.5 Decision Tree python implementation with validation, pruning, and attribute multi-splitting
Contributors: Ryan Madden and Ally Cody

## Requirements
python 2.7.6 [Download](https://www.python.org/download/releases/2.7.6/)

## Files
* btrain.csv, bvalidate.csv, btest.csv - The training, validation, and testing sets used for building and testing the program
* decision-tree.py - The decision tree program
* datatypes.csv - A metadata file that indicates (with comma separated true/false entries) which attributes are numeric (true) and nominal (false) **Note: You must edit this file or supply your own if using a different dataset than the one provided**

## How to run
decision-tree.py accepts parameters passed via the command line. The possible paramters are:
* Filename for training (Required, must be the first argument after 'python decision-tree.py')
* Classifier name (Optional, by default the classifier is the last column of the dataset)
* Datatype flag (-d) followed by datatype filename (Optional, defaults to 'datatypes.csv')
* Print flag (-s) (Optional, causes the dataset)
* Validate flag (-v) followed by validate filename (Optional, specifies file to use for validation)
* Test flag (-t) followed by test filename (Optional, specifies file to use for testing)
* Pruning flag (-p) (Optional, you must include a validation file in order to prune)

#### Examples
#####Example 1
```
python decision_tree.py data/iris_training.arff -t data/iris_test.arff
```
This command runs decision_tree.py with iris_training.csv as the training set and iris_test.csv as the test set. The classifier is not specified so it defaults to the last column in the training set. Printing is not enabled.
#####Example 2
```
python decision_tree.py data/iris_training.arff -t data/iris_test.arff -s
```
This command runs decision_tree.py with iris_training.csv as the training set and iris_test.csv as the test set. The classifier is not specified so it defaults to the last column in the training set. Printing is enabled.
