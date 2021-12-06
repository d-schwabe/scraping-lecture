# Scraping with Beautiful Soup and Selenium

## December 6 lecture

### Terminal things

First, we'll have to install a system-wide package called `chromedriver` via brew. Take a moment to update and upgrade brew before installing.

```sh
% brew update; brew upgrade
% brew install --cask chromedriver
```

You'll have to un-quarantine chromedriver or you'll get an error when you try to use it in Jupyter later.

```sh
% xattr -d com.apple.quarantine $(which chromedriver)
```

Then, we need to pull the newest changes from the `scraping-lecture` repo. Go to the GitHub page for your forked repo (it'll be at https://github.com/username/scraping-lecture, with _username_ replaced with your username).

Click on the dropdown button that says "Fetch upstream"

[Screenshot TK]

Then you'll pull from your repo.

```sh
% cd coding/scraping-lecture
% git pull origin main
```

Did you get the following merge error? 

[Screenshot TK] 

Here's how to fix it. When you're at the above screen, hit the following keys in succession (not simultaneously):
- `ESC`
- `:` (that's a colon; you'll have to also use the SHIFT key)
- `w`
- `q`
- `ENTER`

You'll see that last week's lecture is now in a folder called `pt1`. This week's lecture is in a folder called `pt2`. 

I added a new Python requirement called `selenium` in our [requirements](requirements-3.8.5.txt) file. So you'll need to install the requirements again. Don't forget to activate your virtual environment!

```sh
% pyenv activate scraping-lecture-3.8.5
(scraping-lecture-3.8.5) % pip install -r requirements-3.8.5.txt

# ...
# selenium and other related packages will install
# ...

(scraping-lecture-3.8.5) % jupyter lab
```


## November 30 lecture

### Quick start

First, fork the repo at https://github.com/soooh/scraping-lecture. Then follow these steps, replacing _username_ below with your GitHub username.

```sh
% cd coding
% git clone git@github.com:username/scraping-lecture.git
% cd scraping-lecture
% pyenv virtualenv 3.8.5 scraping-lecture-3.8.5
% pyenv activate scraping-lecture-3.8.5
(scraping-lecture-3.8.5) % pip install --upgrade pip
(scraping-lecture-3.8.5) % pip install -r requirements-3.8.5.txt
(scraping-lecture-3.8.5) % jupyter lab
```

### Notebooks
- [scraping_lecture.ipynb](scraping_lecture.ipynb) 
- [scraping_classwork.ipynb](scraping_classwork.ipynb)
- [scraping_classwork_answers.ipynb](scraping_classwork_answers.ipynb)
