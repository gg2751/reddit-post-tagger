# Reddit Flair Classifier 

[Last Updated: Aug 10, 2021. Commited on June 12, 2024 for Archiving Purposes.]

Reddit Flair Detector for the subreddit 'India' 

<h3> About: </h3>
The Reddit Flair Detector is an application used to detect the flair of a reddit post using the link to the reddit post. The application can be found <a href="https://secure-sands-63470.herokuapp.com/">here</a>.
An endpoint to the application is present at: https://secure-sands-63470.herokuapp.com/automated_testing. An automated post request send to this link will return a json file.

The request can be sent using: 
~~~
import requests

files = {'upload_file': open('file.txt','rb')}
r = requests.post('https://secure-sands-63470.herokuapp.com/automated_testing', files=files)
~~~

<h3> Development Environment: </h3>

1. Download/Clone the repo
2. Run: 
~~~ 
pip install -r requirements.txt
~~~
3. To run the application locally: 
~~~
cd folder-name
py app.py
~~~


<h3> About the Detector: </h3> 

The detector uses scikit's Logistic Regression model for classification of the posts for different flairs of the r/India subreddit. The model uses the posts' title, body (or self-text), comments and url as a combined feature. The accuracy achieved with imputed null values and combined feature is 78-81%. 
