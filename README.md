# INFS-692: Final Project Documentation

**Below is the documentation for the 3 models that this final project is composed of**

## Model 1:

The full model itself is very similar to a reproduction about what happened in week6, where we were asked to perform different classification methods. Since we are asked to have _at least 3 models of our choice_, I have decided to using the stacking methods which suits best for this requirement. The problems detailed step is shown below for me to produce the **ensemble classification model**:

- Implementing all the essential libraries for later processing.
- checking for null and missing values for the data set.
- remove the categorical and binary data to get the **correlation of whole data**.
  - for this one I was first kind of confused, so I removed both `institution` and `Failure.binary`, then attached them both again to the final 2 columns of the data set.
- Doing the training and testing spliting (80% training, 20% testing, and making sure we have the consistent categorical levels first by constructing a blueprint).
- Get the AUC value (which I got 100%) for training.
- Print out the top 20 features using `vip` function.
- Get the AUC value for testing.

I intially thought we are suppose to **compare the `Failure` data with the `Failure.binary` data**, so that we could get the prediction from the comparison. But in the exam I have encountered the same issue, therefore I changed my blueprint parameter back to `Failure.binary`.

## Model 2: A similar reproduction for the **network-based classification** from class

The process is pretty clear by following the instructions on the `FinalProject Instruction` from _myCourses_. For detailed instructions, please read the attached pdf in the GitHub repository. However, I would like to mention that since the `predict_classes` function is unfortunately deprecated from the R library, I have to use `predict` to get the results.

## Model 3: Performing 3 clusting method which is similar from **week 10**

The 3 clustering methods were pretty similar from the week 10 assignment. However, I want to expound on the plotting techniques and problems on the _model-based_ method, since this time the data set has exceed the plot margins in R studio and every time I want to run `plot()` function, it always return the same error to me: `Error in plot.new(): figure margin is too large`. I googled every possible way to solve this problem, turns out it is merely due to the fact that we have 197 rows and 431 columns for the whole dataset. For the assignment in week 10, we only have 4 columns. Therefore, I chose 4 different columns to perform the clustering on Entropies and Failure(`Failure`, `Entropy_cooc.W.ADC`, `Entropy_hist.PET`, and `Entropy_cooc.L.PET`) and I was able to reproduce all the results in the week 10 assignment for model-based method.

**However**, just in case that some one want to know the model based clustering on the entire dataset, I also performed the same process without implementing the `plot()` functions so that you can get essential numbers and results for the clustering.

**_Notice_**: while kniting my Rmd file to a PDF version, an LaTex Error occurred saying I am using unicode U+001B. In my Rmd file there is no known graph that I have implemented the `esc` or `^` feature. I don't know how this occurred so I finally knit the Rmd file to an HTML and then transform the HTML to a PDF. Therefore, the output format might be a little different. For a more detailed reference, I have included both HTML and PDF file for Model 3.

And that shall be the end of INFS 692 final project 🥰.
