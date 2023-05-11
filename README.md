## Setup Python env.

- We will use Python 3 with a virtual environment Using one, you can separate projects that have different needs. For example, you might use one virtual environment for projects involving packet inspection and a different one for projects on binary analysis.

- By having separate environments, you keep your projects simple and clean. This ensures that each environment can have its own set of dependencies and modules without disrupting any of your other projects.

### Lets create Virtual env.

`sudo apt install python3 python3-venv`\
`python3 -m venv chap1`\
`source chap1/bin/activate`\
`deactivate`                  (to deactivate the virtual env, do this while exiting the program)

If you are too lazy to type python3 instead of python, then use this\
`sudo ln -s /usr/bin/python3 /usr/bin/python`

- when the venv is active, if you use pip, then the package is stored only in venv.\
`pip install hashcrack`

- To check if the package is perfectly installed, drop a python shell and import the package.\
`python3`\
`import hashcrack`

- If not perfectly installed, then it throws this error\
`Traceback (most recent call last):`\
`  File "<stdin>", line 1, in <module>`\
`ModuleNotFoundError: No module named 'hashcrack'`

- Install an IDE\
`apt-get install code`    (From web)\
`apt-get install -f ./code_1.39.2-1571154070_amd64.deb`  (From a file)

## Code Hygiene

- Follow the guideline from PEP 8\
`https://www.python.org/dev/peps/pep-0008/.`

### To summarize
- Keep imports in order to avoid double imports
- Use classes instead of functions if you have a data structure to use multiple times.
- Be good at naming the variables.