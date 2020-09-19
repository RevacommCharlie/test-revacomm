# Python Code Snippet Challenges

Code Snippet Challenges allow a student to write Python directly in Learn. The submission is evaluated against unit tests that are setup as part of the Challenge. The student then sees the standard output from the test runner in Learn.

## Interactive Example

### !challenge

<!-- type is required, type of challenge -->
<!--'language' is required for type: code-snippet. For python, options are 'python2.7' and 'python3.6' -->
<!-- id is required -->
<!-- title is required -->

* type: code-snippet
* language: python2.7
* id: e507c4d0-ee10-4d0e-bf02-76fd422e3578
* title: filter by class

<!-- !question is required -->

### !question

Implement the function `filter_by_class`: It takes a feature matrix, `X`, an array of classes, `y`, and a class label, `label`. It should return all of the rows from X whose label is the given label.

```python
>>> X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
>>> y = np.array(["a", "c", "a", "b"])
>>> filter_by_class(X, y, "a")
array([[1, 2, 3],
       [7, 8, 9]])
>>> filter_by_class(X, y, "b")
array([[10, 11, 12]])
```
### !end-question

<!-- !placeholder is optional, the starter code that will be added to the editor -->

### !placeholder

```python
def filter_by_class(X, y, label):
    '''
    INPUT: 2 dimensional numpy array, numpy array, object
    OUTPUT: 2 dimensional numpy array

    Return the rows from X whose corresponding label from y is the given label.
    '''
    pass
```
### !end-placeholder

 <!-- !tests are required -->

### !tests
```python
import unittest
import main as p		
import numpy as np

class TestChallenge(unittest.TestCase):
  def test_filter_by_class1(self):
      X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
      y = np.array(["a", "c", "a", "b"])
      result = p.filter_by_class(X, y, "a")
      answer = np.array([[1, 2, 3], [7, 8, 9]])
      assert np.array_equal(result, answer)

  def test_filter_by_class2(self):
      X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
      y = np.array(["a", "c", "a", "b"])
      result = p.filter_by_class(X, y, "b")
      answer = np.array([[10, 11, 12]])
      assert np.array_equal(result, answer)
```
### !end-tests

### !hint

Here are the tests:

```python
import unittest
import main as p		
import numpy as np

class TestChallenge(unittest.TestCase):
  def test_filter_by_class1(self):
      X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
      y = np.array(["a", "c", "a", "b"])
      result = p.filter_by_class(X, y, "a")
      answer = np.array([[1, 2, 3], [7, 8, 9]])
      assert np.array_equal(result, answer)

  def test_filter_by_class2(self):
      X = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]])
      y = np.array(["a", "c", "a", "b"])
      result = p.filter_by_class(X, y, "b")
      answer = np.array([[10, 11, 12]])
      assert np.array_equal(result, answer)
```

### !end-hint

### !hint

Use the chat bubble in the lower right corner to ask your instructor for help.

### !end-hint

<!-- !explanation is optional, shown after the student answers correctly -->

### !explanation

```python
def filter_by_class(X, y, label):
    return X[y == label]
```
### !end-explanation

### !end-challenge

## Dependencies

Here's what is installed and ready to use. Want to see something else? Reach out on the #Learn channel.
```
Python 2.7 or Python 3.6 (defined in markdown, see example)

installed--
appdirs==1.4.2
cycler==0.10.0
functools32==3.2.3.post2
keras=2.0.2
matplotlib==2.0.0
nltk==3.2.2
numpy==1.10.1
packaging==16.8
pandas==0.19.2
pip==9.0.1
psycopg2==2.7.1
pymc==2.3.6
pyparsing==2.1.10
python-dateutil==2.6.0
pytz==2016.10
scikit-learn==0.18.1
scipy==0.19.0
setuptools==34.3.0
six==1.10.0
sklearn==0.0
subprocess32==3.2.7
tensorflow=1.0.0
virtualenv==15.1.0
wheel==0.29.0

Contents of ~/.keras/keras.json--
{
    "floatx": "float32",
    "epsilon": 1e-07,
    "backend": "tensorflow"
}
```

## Markdown

Challenges are written inline in markdown content in Learn.  
