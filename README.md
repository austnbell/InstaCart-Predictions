# InstaCart-Predictions

For my first machine learning project, I chose to do an old Kaggle competition.  The goal of the competition hosted by InstaCart was to utilize a portion of de-identified data to predict a user's next order.  The competition required a submission of 75,000 users tand their predicted next orders.  The submission was ranked via the highest F1 score.

In this project, I conduct three groups of analyses: an exploratory data analysis, a customer segmentation analysis, and, finally, developed a model predicting each users' orders.  

There are some caveats to the model presented - primarily, there were many possible feature or the like that I chose to exclude in an effort to learn as much as possible for my first large scale analysis.  This included leaving out many features that were presented by Kagglers in the top 100 that would have led to a much stronger model. In addition, I have not included a script that allowed the user to maximize the F1 score in a similar method as InstaCart for their final grading. Finally, I limited my model to a about two dozen core features due to laptop restictions. 

I conducted the following three analyses:
1) Basic exploratory data analysis - visual and tables to better understand the data
2) Customer segmentation - goal was to group customers together based on past orders and likelihood to reorder. Ran Principal Components analysis to reduce number of product groups then grouped users via K-means clustering.
3) Final script generates a series of features based on the user, product, and user by product. Uses GridSearchCV in order to tun parameters, uses cross-validation to identify the optimal threshold for the highest F1 score, and finally trains a Light GBM model. 

