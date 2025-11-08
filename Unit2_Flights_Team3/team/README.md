How to Run Instructions: 

1. Download the Kaggle flights dataset. See the link in the Dataset choice section.
2. Manually upload the flights dataset to BigQuery by creating a GCS bucket.
3. Under your project ID in BigQuery, create a dataset and label it “assignment2”.
4. Create a table inside the “assignment2” dataset and label it “flights”. Upload the contents of the flights dataset from the GCS bucket onto this table.
5. Download the Unit2_BQML_Flights_Classification_Template.ipynb from the course GitHub page and upload it to Google Colab.
6. Use this downloaded notebook to conduct your analysis by running the cells.
7. Read through every cell, and in the first step, give your specific project ID and table path to access the Kaggle downloaded flights dataset from BigQuery.
8. Complete and run all the steps in the notebook. Use Gemini to debug your code.
9. After each step generates the required output, write a short reflection explaining what the code accomplishes, its results, and its interpretation.
10. After all the cells have been executed, complete the “Write-up” section, towards the end of the notebook. Answer each section based on the output generated in each step.
11. Upload your individual completed notebook to the individual folder in the team GitHub page.
12. Create an Operations Brief and share it with all team members so that they can contribute as well.
13. Create a README file in the team folder of the team's GitHub page.
14. Complete the Operations Brief and upload it as a PDF to the team folder of the team’s GitHub page.
15. Once all the deliverables in the assignment have been completed, follow the instructions in BrightSpace to upload all the assignment 2 materials.
16. Submit Assignment 2 in BrightSpace.
    
Dataset Choice: We chose to analyze a flights dataset from Kaggle because the 2 flights datasets in BigQuery were not available. Here is the link to the dataset from Kaggle: https://www.kaggle.com/datasets/usdot/flight-delays?select=flights.csv  

Assumptions: This flights dataset contains the same columns and is the most similar to the BigQuery flights datasets. This assumption helped us perform our analysis, as the dataset contains all the relevant columns needed for training and testing the baseline and all the engineered models. 

