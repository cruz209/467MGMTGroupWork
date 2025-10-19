Reproducibility instructions: 

Download the Jupyter notebook from the class’s Brightspace page. 
Insert a mix of text and code cells into the notebook. 
In the text cells, start by writing the assignment 1 name, project title, dataset name, objective, and deliverable. Go to the class’s Brightspace page for this relevant information. 
First, connect the Google Colab to BigQuery using the gemini-generated code to authenticate this connection. This will help to load and access the datasets from BigQuery into Google Colab. 
Ensure that the datasets have been loaded through print statements and displaying the first 5 rows of each of the tables as pandas dataframes in Colab notebook through Gemini-generated codes. 
Then, perform the DIVE Analysis. Dedicate each text cell to one part of the DIVE. For example, one text cell contains all instructions for D: discover. These instructions can be copied and pasted into the Colab notebook from the course’s Brightspace page. Then, repeat the same for I: investigate, V: validate, and E: extend (communicate). 
After each text cell, insert code cells and use Gemini to perform each step of the DIVE Analysis. The sample prompts to enter into Gemini can be found in the prompts_log file. 
After each step of the DIVE Analysis, insert a text cell and write your reflection for that step, indicating your key findings. This should be based on the outputs generated in the code cells. 
After DIVE Analysis is completed, log in to Looker Studio and re-create the visualizations created using Plotly in the colab notebook in the Looker Studio Dashboard. Share this dashboard with all team members so that they can create their visualizations too. 
After the Looker Studio Dashboard is completed, write a 1-page MD summary that demonstrates what you found, what changed after validation, and what you propose. This summary should be based on the results found in the DIVE Analysis. 
Create an Executive Brief Word document and share it with all team members for them to contribute as well. 
In the Executive Brief document, write the integrated story of the dataset, supporting it through evidence found using the DIVE Analysis. Also, include images from the colab notebook to show your findings. Make sure the document is between 2-3 pages and is converted to a PDF file when completed. 
Upload your final Colab notebook and MD summary to the individual sub-folder of the Unit1_TheLook_Team3 folder in the team repository GitHub page. 
Create a prompts_log.md file in the team sub-folder and include key prompts used across team members. Also include 2 “fail then fix” prompt examples when generating your code using Gemini in Colab notebook during DIVE Analysis. 
Upload the Executive Brief as a PDF file to the team subfolder. 
Submit Assignment 1 through a single ZIP folder, including Looker Studio Dashboard and team repository links. 

Dataset References: 

Dataset used: bigquery-public-data.thelook_ecommerce
Table names in the dataset used: users, products, orders, order_items, inventory_items, events, distribution_centers.  
