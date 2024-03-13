# deep-learning-challenge
#Purpose: The purpose of this analysis is to use deep learning to create a model that will predict a binary outcome (yes/no) of what applicants of Alphabet Soup will receive funding based on numerous features.
#Results:
- Data Preprocessing:
  Targets were identified at 0 (did not receive funding) or 1 (received funding). Features included everything that was not tied to an ID (ex. name or EIN). features that were
  heavily dominated by one value were removed (STATUS and SPECIAL CONSIDERATIONS).

- Compiling, Training, and Evaluating the Model:
  For my first layer, I selected 86 neurons because this was double the amount of features that were in the training set. The middle 2 layers had 43 neurons (these were arbitrary).
  My final layer had 1 neuron activated by the sigmoid funcitons to give a 1 or 0 recommendation. All preceding layers used the tanh function because those generated better model
  accuracy than the relu function.
  The test set acheived 72.99% accuracy which is the best I could achieve. I started off using the relu function for my layers. Switching to tanH had roughly 1% improvements.
  Removing STATUS and SPECIAL_CONSIDERATIONS gathered roughly .1% improvements in test set accuracy. I tried using the Keras tuner briefly but I found it to be a lengthy process to
  run for the purposes of this assignment so I stuck with my layers/neuron configurations listed above.

- Summary:
  Overall the test set can predict wit 73% accuracy whether or not an applicant will receive funding. A decision tree ML model could also be worth using to predict applicant
  success. Errors in the ML model could then be traced back through a decision tree.
