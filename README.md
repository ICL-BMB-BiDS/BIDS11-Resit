# Assignment_Data for the resit

Please refer to the recording of BIDS11 for additional details.
_Note that this is a different dataset than what was used in BIDS 2025, i.e. *do not* use the data in [BIDS11-AssignmentData](https://github.com/ICL-BMB-BiDS/BIDS11-AssignmentData)._

With the materials from BIDS2-10 you are tasked to:
-	Create a data analysis workflow to best classify non-IBD, Crohn’s Disease (CD) and Ulcerative Colitis (UC) samples using at least 1 method from BIDS 2-4 (dimension reduction), at least 1 method from BIDS 5-6 (clustering) and at least 1 method from BIDS 7-10 (supervised learning).
-	Give a measure of variable importance to individual variables *for each group*.

To answer two research questions:
1.	How well can you predict new samples to be either a Crohn’s disease, ulcerative colitis or control sample using a data analysis workflow that includes methods from BIDS 2-4, BIDS 5-6 and BIDS 7-10?
2.	What are the (most) predictive variables of your model *for each group*?

The resit training dataset has 417 different samples and all materials (including the test set and submission format) for the assignment can be found here:
- BIDS_assignment_training_data_RESIT.xlsx
- BIDS_assignment_test_data.xlsx
- BIDS_assignment_test_data_predictionsubmissionformat.xlsx

Create a Jupyter Notebook using your choice of tutorial materials from BIDS2-10 to predict the unlabelled test set, ensure the file for summative submission is created as described on the GitHub/in BIDS11:
1. Use BIDS_assignment_training_data_RESIT.xlsx to train your models.
2. Apply your model on BIDS_assignment_test_data.xlsx.
3. Add your test set predictions in BIDS_assignment_test_data_predictionsubmissionformat.xlsx.

<!-- If your CID is 01234567 and you are submitting for formative feedback: -->
<!-- 4. Save this file as BIDS_2024_01234567_test_predictions_formative.xlsx -->

<!-- If submitting for summative assessment of the coursework: -->
To submit for summative assessment of the coursework, and your CID is 01234567:

<!-- 5. Save this file as BIDS_2025_01234567_test_predictions_summative.xlsx -->
4. Save this file as BIDS_2025_01234567_test_predictions_summative.xlsx

<!-- Instructions of how to receive formative feedback are provided in BIDS 11 (and re-iterated in BIDS 12). -->

Here is some example code how you can do this:
```
# change this to the location of the submission file (in folder of assignment data)
Y_pred_format = pd.read_excel('BIDS_assignment_test_data_predictionsubmissionformat.xlsx')
# change this variable (y_pred_test) to whatever you named the predicted class of the assignment test data
Y_pred_format.Predicted_Group = y_pred_test
# change this to YOUR CID number
CID = '1234567'
# change this for the type of submission (formative or summative)
tp = 'summative'

# do not change anything below
filename1 = 'BIDS_2025_' # do not change this
filename2 = '_test_predictions_' # do not change this
filename3 = '.xlsx' # do not change this
filename = filename1+CID+filename2+tp+filename3 # do not change this
# save the predictions in the format you need to email me (is saved in the folder of the notebook)
Y_pred_format.to_excel(filename)
```
