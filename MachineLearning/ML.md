
he's identified price patterns from houses he has seen in the past, and he uses those patterns to make predictions for new houses he is considering
This step of capturing patterns from data is called fitting or training the model

 how the model is fit (e.g. decision tree : how to split up the data ? )


Here's the takeaway: Models can suffer from either:

Overfitting: capturing spurious patterns that won't recur in the future, leading to less accurate predictions, or
Underfitting: failing to capture relevant patterns, again leading to less accurate predictions.
We use validation data, which isn't used in model training, to measure a candidate model's accuracy. This lets us try many candidate models and keep the best one
