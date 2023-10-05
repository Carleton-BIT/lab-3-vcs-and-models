# lab-3-vcs-and-models

## Steps to get this django app running on your own server
0) Hello Eveyone this is Agnes, I am making edits to the readme nive to meet whoever is reading this
:))))))))))))))))))))))))))))))))

1) Open a terminal and navigate to the folder you want to create your project in (e.g. `cd ~Documents/Code`)
2) Clone this repository with `git clone https://github.com/Carleton-BIT/lab-3-vcs-and-models.git`
3) Open the repository with PyCharm. You can do this by going file->open and selecting the cloned folder called `lab-3-vcs-and-models`
4) Configure your project interpreter. Go to file->settings, and selecting Python Interpreter under `Project: lab-3-vcs-and-models`, and clicking Add Interpreter->Add Local Interpreter
![screenshot for adding interpreter](readme_assets/add-interpreter.PNG)
5) Choose the default settings and click OK
![screenshot for virtualenv settings](readme_assets/confirm-interpreter.PNG)
6) Then, you can install dependencies using PyCharm (django and python-decouple). Or, you can use the command line (`pip install django python-decouple`)
![screenshot for adding dependencies](readme_assets/add-dependencies.png)
7) Create a run configuration:
![edit run configs](readme_assets/edit-run-configuration.png)
8) Configure it to run manage.py with the parameter runserver:
![finished run config](readme_assets/finished-run-configuration.png)
9) In your project folder (lab-3-vcs-and-models/studentdemo) create a file called `.env`
10) Generate a secret key by running `python -c 'from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())'` in the terminal. Copy the output.
11) Edit `.env` (created in part 9) with a text editor like notepad, and add a line that says `SECRET_KEY="your-secret-key-here"`. Paste the output from part 10 into 'your-secret-key-here'.
12) On the terminal, navigate to `lab-3-vcs-and-models/studentdemo` and run `python manage.py migrate`
13) Run the server by clicking the play button for the run configuration you set up
14) Navigate to 127.0.0.1:8000! Your app should load.
