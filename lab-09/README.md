# Lab Overview

[Azure Machine Learning designer](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-designer) (preview) gives you a cloud-based interactive, visual workspace that you can use to easily and quickly prep data, train and deploy machine learning models. It supports Azure Machine Learning compute, GPU or CPU. Machine Learning designer also supports publishing models as web services on Azure Kubernetes Service that can easily be consumed by other applications.

In this lab, we will be compare the performance of two different multiclass classification approaches: `Two-Class Support Vector Machine` used with `One-vs-All Multiclass` module vs `Multiclass Decision Forest`. We will apply the two approaches for the letter recognition problem and compare their performance. We will do all of this from the Azure Machine Learning designer without writing a single line of code.

# Exercise 1: Create Training Pipeline

## Task 1: Open Sample 12: Multiclass Classification - Letter Recognition

1. In [Azure portal](https://portal.azure.com/), open the available machine learning workspace.

2. Select **Launch now** under the **Try the new Azure Machine Learning studio** message.

    ![Launch Azure Machine Learning studio.](images/01a.png 'Launch AML')

3. When you first launch the studio, you may need to set the directory and subscription. If so, you will see this screen:

    ![Launch Azure Machine Learning studio.](images/00.png 'Launch AML')

    > For the directory, select **Udacity** and for the subscription, select **Azure Sponsorship**. For the machine learning workspace, you may see multiple options listed. **Select any of these** (it doesn't matter which) and then click **Get started**.

4. From the studio, select **Designer, Show more samples**.

   ![Image highlights the steps to open the sample pipeline, Sample 12: Multiclass Classification - Letter Recognition.](images/01_1.png 'Samples Page')

5. Select **Sample 12: Multiclass Classification - Letter Recognition**.

   ![Image highlights the steps to open the sample pipeline, Sample 12: Multiclass Classification - Letter Recognition.](images/01_2.png 'Samples Page')

## Task 2: Setup Compute Target

1. In the settings panel on the right, select **Select compute target**.

    ![Image highlights the link to select to open the setup compute target editor.](images/02.png 'Setup Compute Target')

2. In the `Set up compute target` editor, select the available compute, and then select **Save**.

>> Note: If you are facing difficulties in accessing pop-up windows or buttons in the user interface, please refer to the Help section in the lab environment.

   ![Image shows how to select the existing compute target named qs-compute.](images/03.png 'Setup Compute Target')

# Exercise 2: Submit Training Pipeline

## Task 1: Create Experiment and Submit Pipeline

1. Select **Submit** to open the `Setup pipeline run` editor.

    ![Image shows where to select the submit button to open the setup pipeline run editor.](images/07.png 'Submit Pipeline')

    > Please note that the button name in the UI is changed from **Run** to **Submit**.

2. In the `Setup pipeline run editor`, select **Experiment, Create new** and provide `New experiment name:` **letter-recognition**, and then select **Submit**.

    ![Image shows how to provide the experiment name in the setup pipeline run editor and start the pipeline run.](images/08.png 'Submit Pipeline')

3. Wait for pipeline run to complete. It will take around **10 minutes** to complete the run.

4. While you wait for the model training to complete, you can learn more about the `One-vs-All Multiclass` module used in this lab by selecting [One-vs-All Multiclass](https://docs.microsoft.com/en-us/azure/machine-learning/algorithm-module-reference/one-vs-all-multiclass).

# Exercise 3: Compare Model Performance

## Task 1: Open Evaluation Results

1. Select **Evaluate Model, Outputs, Visualize** to open the `Evaluate Model result visualization` dialog.

    ![Image shows how to open the evaluate model result visualization dialog.](images/09.png 'Evaluate Model Results')

## Task 2: Compare Performance Metrics

1. Select the regression performance metric **Overall_Accuracy** and compare performance of the two algorithms: `Two-Class Support Vector Machine` and `Multiclass Decision Forest`.

    ![Image shows the evaluate model result visualization dialog.](images/10.png 'Compare Performance Metrics')

## Task 3: Conclusion

1. The `Two-Class Support Vector Machine` algorithm is extended for multiclass classification problem by using the `One-vs-All Multiclass` module.

2. As you can observe that the native multiclass algorithm `Multiclass Decision Forest` outperforms the `Two-Class Support Vector Machine` across all key performance metrics.

3. One recommendation for next steps is to increase the `Number of iterations` parameter for the  `Two-Class Support Vector Machine` module to an higher value like **100** and observe its impact on the performance metrics.

# Next Steps
Congratulations! You have trained and compared performance of two different multiclass classification machine learning models. You can continue to experiment in the environment but are free to close the lab environment tab and return to the Udacity portal to continue with the lesson.
