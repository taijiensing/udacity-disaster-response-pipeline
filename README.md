# udacity-disaster-response-pipeline
This Project is part of Data Science Nanodegree Program by Udacity in collaboration with Figure Eight. The dataset contains pre-labelled tweet and messages from real-life disaster events. The project aim is to build a Natural Language Processing (NLP) model to categorize messages on a real time basis.

The project is divided into 3 main parts:

   1. Pre-process data, build an ETL pipeline to extract,clean data from source, and save it in SQLite DB format.
   2. Build a machine learning pipeline to train a model to classify text messages by respective categories.
   3. Run a web app that shows classification of results in real time

# Installation:
Clone the git repository:

    git clone https://github.com/taijiensing/udacity-disaster-response-pipeline.git

# Executing the Program:

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
    
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
        
    - To run ML pipeline that trains classifier and saves
    
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/

   ![alt text](https://github.com/taijiensing/udacity-disaster-response-pipeline/blob/master/screencaps/troubleshoot1.png?raw=true)

# Additional Troubleshooting:
1. When working out of udacity workspace, http://0.0.0.0:3001/ was not able to load.

   ![alt text](https://github.com/taijiensing/udacity-disaster-response-pipeline/blob/master/screencaps/troubleshoot2.png?raw=true)

2. To resolve this, once app in running (python run.py):

    - Open another terminal and type:
    
        `env|grep WORK`
            
    - This will show something along the lines of SPACEID=view******** (combination of digits and characters)

   ![alt text](https://github.com/taijiensing/udacity-disaster-response-pipeline/blob/master/screencaps/troubleshoot3.png?raw=true)

    - Open browser window and type:
    
        `https://view********-3001.udacity-student-workspaces.com`
            
    -  Press enter and the app should now execute.

# Important files

### Data Folder
1. process_data.py: Read, clean, and store data in SQL DB.
2. disaster_categories.csv: Dataset
3. DisasterResponse.db: Resulting database from process_date job

### Models Folder
1. train_classifier.py
2. classifier.rar: Compressed classifier.pkl file

### App Folder
1. run.py: Flask app with UI to predict results and display them.
2. templates: folder containing html templates

# Screenshots
1. Example of a message to indicate hunger: 'I am hungry!'

   ![alt text](https://github.com/taijiensing/udacity-disaster-response-pipeline/blob/master/screencaps/search-hunger.png?raw=true)
   
2. Example of a message to indicate hunger: 'Everyone is sick!'

   ![alt text](https://github.com/taijiensing/udacity-disaster-response-pipeline/blob/master/screencaps/search-sick.png?raw=true)

3. Visualizing Figure Eight's dataset: 

   ![alt text](https://github.com/taijiensing/udacity-disaster-response-pipeline/blob/master/screencaps/data-visualisation.png?raw=true)
