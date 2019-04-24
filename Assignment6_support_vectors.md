## Question
Question about the SVM examples: in the first example (In [3]), why are the support vectors inside the margin? Isn't the point of SVM (before relaxing C anyway) to create a maximum margin between the support vectors and the decision line?


## Answer

- If you check the [documentation](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html), C = 1 by default. The C parameter controls how strict you would like your margins to be, as we see under Regularization (In [4]:). C = 1 is strict, but not as strict as C = 1,000,000. In this case, the support vectors are inside the margin because C = 1 is not strong enough to push them out. 
- The point of SVM is to create a decision boundary (cat/dog, tumor/no tumor)
  for your dataset. It creates the boundary by maximizing the distance from the
  support vectors.
    - Here is the procedure for creating an SVM, roughly:
        - find support vectors allowed by C parameter
        - choose the boundary that maximizes the distance from the boundary to the
          support vectors
- [Andrew Ng on SVM](https://www.youtube.com/watch?v=hCOIMkcsm_g)
