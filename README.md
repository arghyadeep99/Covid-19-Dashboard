<h1 align="center">🇮🇳 :robot: Covid-19 Dashboard 🦠:warning: </h1>

<div align="center">

<img src="./logo.jpg" width=250px height=225px/>

<br>

[![](https://img.shields.io/badge/Made_with-Python3-red?style=for-the-badge&logo=python)](https://www.python.org "Python3")
[![](https://img.shields.io/badge/IDE-Visual_Studio_Code-red?style=for-the-badge&logo=visual-studio-code)](https://code.visualstudio.com/  "Visual Studio Code")
[![](https://img.shields.io/badge/Deployed_on-Slack-red?style=for-the-badge&logo=slack)](https://www.slack.com/  "Slack")

<br>

</div>

---

<h2>Motivation:</h2> 

It's quarantine phase in India and every CS enthusiast is determined to help in some technical way to fight this pandemic called Covid-19. Hence, it motivated me to try something in terms of chatbot to keep me updated about live changing numbers since different media channels show different count of patients. This chatbot fetches Corona patients data from official website of Government of India and returns information about the state-wise patients automatically in #random channel. 

### Goals of this project:

* [x] Learn chatbot development (at least rule based)
* [x] Learn how to deal with external APIs in Slack. 
* [x] Learn web scraping using Beautiful Soup. 
* [x] Cut out boredom during this quarantine phase. 

---

<h3 align="center">Chatbot in Action</h3>

<div align="center">
<img src="./ss.png"/>
<br>
</div>

---
#### To talk with my chatbot, kindly join my Slack [here](https://join.slack.com/t/arghyadeep/shared_invite/zt-ctlwd1oh-OCSpzwTsbSoEJZ1gWhm5Qw) and go over to #random channel to talk with it. 

### To run this Project:

* Create an account on Slack and create your own workspace. 
* Clone this repo, pip install the requirements and create auth.py:
```bash
git clone https://github.com/arghyadeep99/Go-Karuna-Go.git
cd Go-Karuna-Go
pip install -r requirements.txt
touch auth.py
```
* Set up your Slack API by creating an app and allow incoming webhooks.
* Copy your Slack webhook and put it in auth.py:
```python
DEFAULT_SLACK_WEBHOOK = 'https://hooks.slack.com/services/<your webhook url>'
```
* Setup a cronjob to receive updates whenever there's a change on government website. 
```bash
crontab -e # opens an editor like vim or nano
# now write the following line in the crontab file:
*/5 * * * * python3 $PATH_TO_GO_KARUNA_GO/corona-bot.py --states 'haryana,maharashtra'
# Replace $PATH_TO_GO_KARUNA_GO with actual path to the python file.
# /5 indicates job will run every 5 minutes
# In order to receive updates for all states, ignore the --states flag
```

### Future scope of this project:

* [ ] Add ability to query for FAQs regarding Corona Virus from authentic sources like WHO. 
* [ ] Incorporate this bot as a service on my [website](https://arghyadeep99.github.io).  

### Tech Stack of this Project:

* Backend: Python3
* Dependencies: Slack API
* Libraries: Available in [requirements.txt](https://github.com/arghyadeep99/Go-Karuna-Go/blob/master/requirements.txt).


#### This project still has scope of development, so you can also contribute to this Project as follows:
* [Fork](https://github.com/arghyadeep99/Go-Karuna-Go) this Repository.
* Clone your Fork on a different branch:
	* `git clone -b <name-of-branch> https://github.com/arghyadeep99/Go-Karuna-Go.git`
* After adding any feature:
	* Goto your fork and create a pull request.
	* I will test your modifications and merge changes.

This project was done `in my quarantine time as a concerned citizen of India, willing to contribute in some way.`

---
<h3 align="center"><b>Developed with :heart: by <a href="https://github.com/arghyadeep99">Arghyadeep Das</a>.</b></h1>

