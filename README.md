# CSE6242 Team 76 Project (Fall 2020)

Our course project is to help the users better analyse and visualize the US car accident dataset. The users can also predict the car severity based some features loaded from the web-app interface. 

By Cong Wang, Fang Fu, Ruiqiang Chen, Xuebing Xiang, Yao Lu, and Yu Chen. 

## Required Dependencies

- Please install the Flask, Pandas and scikit-learn libraries in order to use our application. Relevant links are available below:

(https://pandas.pydata.org/pandas-docs/stable/install.html)

(http://flask.pocoo.org/docs/0.12/installation/)

(https://scikit-learn.org/stable/)

- An easy way to install all dependencies is run *pip3 install -r requirements.txt* once you clone the repo and change directory to the main directory of the repo/project. 

## Webapp Installation and Launch

- You can choose to download the for this repository to your system or use terminal:

```
git clone https://github.gatech.edu/rchen413/CSE6242_team76_project
```

- Some files with size larger than 100 MB are not included in the Git repo, like the precessed datasets (dataset_featureviz.csv files) and trained models (15wRF_limit.pickle and 15wXGB_limit.pickle). Please download them from [this Google shared drive](https://drive.google.com/drive/folders/11G-OWjtxEsZ6_sLuW03AQNa4mlvdiTS5). After downloading, please **save that .csv file into the app foler /static/data directory and save the two .pickle files to /models/ directory. If may need to create the models directory if you do not see it in the clone structur**.

We also recommend reviewing the website on Kaggle <a href="https://www.kaggle.com/sobhanmoosavi/us-accidents/" target="_blank">here</a> that helps understand the various columns/attributes of the data.

After above operation the structure of files in the Flask based webapp should be like this:

```
├── README.md
├── app.py
├── extralib
│   ├── jquery-2.1.4.min.js
│   └── socket.io.js
├── models
│   ├── 15wRF_limit.pickle
│   ├── 15wXGB_limit.pickle
├── requirements.txt
├── static
│   ├── css
│   ├── data
│   ├── img
│   ├── js
│   └── lib
└── templates
    ├── about.html
    ├── dataset.html
    ├── explore.html
    ├── featureviz_YC.html
    ├── index.html
    ├── severitybycounty1_YC.html
    └── severitybyyear_YC.html
```

- Open terminal and change working directory to the main directory of the CSE6242_team76_project directory. **Please make sure required dependencies were correctly installed!** Run the program *app.py* in python:
```
python app.py
```
- If flask has been installed as stated above and there are no other errors (hopefully!), then you should see something like this in your terminal:
```
* Debug mode: on
* Running on http://localhost:6242/ (Press CTRL+C to quit)
* Restarting with stat
* Debugger is active!
* Debugger PIN: xxx-xxx-xxx
```
- Now open a browser of your choice (we like Firefox; Chrome, Safari distort our beautiful work), and type in http://localhost:6242/ to your search bar. You should have reached the landing page of the project. Congratulations!

## User interface introduction

- “Severity Prediction” tab includes a short description about the model used for prediction of the
new data and a simple tutorial on how to use. In the second part, it allows the users to input new accident
data and choose the model to predict severity level. 

- “Explore & Visualize” tab includes interactive choropleth maps and data statistics. It provides interacitve and static data visualization to help the users better understand the car accidents in US. When you click the and the link "U.S. Accidents Dataset Feature Visualization" it will usually take about 5-10 seconds to see plot displayed on the browser as the datasets processed by backend is large, more than 1 million rows. 

- “About Dataset” tab includes a sample plot, the description and source of the datasets.

- “Team Introduction” tab includes the project description and team member information.


If you find errors with our implementation, please submit a pull request on our Github page. If you want to build-upon our work, fork us (and star us if you appreciate our work!).

## FAQs

- How to send feedback to the developers?\
  In the “Team Introduction” tab you can send email to the developer by clicking developer's name. 
