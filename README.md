# Feature Scaling on Mobile Price Classification problem

The scope of this works includes 2 distance-based models, which are KNN and SVM, and experiment how scaling features affects the performance of these 2 models. The work is conducted under the context of Mobile Price Classification dataset from Kaggle.

During the visualization, I found out that `ram` has the most correlation towards the target `price`.
The result shows that:
- For KNN classifier, if we do not scale the features, the model performs much better. The reason for this is because the `ram` feature may contributes a lot towards the target. Also, the scale of `ram` is much bigger comparing to other features (based on median, min, max values and std). Therefore, scaling all the features into the same scale (range 0-1) will weight down the importance of `ram`.
- For SVM classifier, with linear kernel, if we do not scale the features, the model takes a huge amount of time for training. In other hand, if we scale the feature, SVM performs much better (comparing to KNN) and faster. For non-linear SVM, the model performs slightly worse comparing to linear kernel one.

For more details, feel free to reference the .ipynb file and give feedbacks.