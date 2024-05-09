# Trees-and-Forest (in R)

## Example of Regression trees and Random Forest application 
Welcome! In this repo, we will see how use the Random Forest to estimate the component of the insurance Pure Premium: claims frequency and claims severity.
We saw how the CART algorithm works in a previous repo. 


We will explain the pros and cons of each method, tackling the hyper-parameter tuning strategy process. 
![Example of real tree](https://github.com/william-tiritilli/Trees-and-Forest/assets/46381506/e256ca82-f0a3-43e1-86d7-b998e6f81c58)

## Data
The data in use come from the chapter one of the book “Predictive Modelling Applications in Actuarial Science, Vol.2”, Edited by E. Frees et al.. A textbook for people who wants to develop knowledge in these fields.
The book's website is located here: https://instruction.bus.wisc.edu/jfrees/jfreesbooks/PredictiveModelingVol1/glm/v2-chapter-1.htm

## Explanations
RF is an extension of Bagging. The difference is that before each split, the algorithm selects randomly a subset of features as "features candidate" for splitting. Hence, it de-correlates the trees and helps to improve the predictive performance.
-	Step 1: Create a bootstrapped data set from the original data set. It is done by randomly selecting sample from the original data with replacement. In general, 1/3 of the original data don't end up in this bootstrapped data set. We call it the "Out-of-Bag" data set (a.k.a "OOB"), referring to the entries that have not been selected to compose the original bootstrapped data set.
-	Step 2: create a decision tree using the bootstrapped data set, but only considering a random subset of variables at each step. It follows the same logic as a single tree, but this time we select a random number of variables.
-	Step 3: repeat steps 1 and 2 a certain number of time. It results in a wide variety of trees which makes the random forest more effective than an individual tree. 

## Conclusion
Powerful out-of-the-box algorithm that often has great predictive accuracy. 
Add the benefits of decision trees  and bagging but greatly reduce instability and between-tree correlation.
However, suffer from slow computational speed as your data sets get larger.
![image](https://github.com/william-tiritilli/Trees-and-Forest/assets/46381506/d56cc9d6-16dc-4c59-979b-2ce97520c9e5)


