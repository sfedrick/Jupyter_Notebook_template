This is a collection of jupyter notebooks used for quick python code snippets or analysis.

run this in the command line
'''
. activate.sh
'''

Place all jupyter notebooks you don't want version controlled in sandbox folder.

you can then use voila to serve these jupyter notebooks as apps
voila <path-to-notebook> <options>
For example, to render the bqplot example notebook as a standalone app, run
cd voila
voila notebooks/bqplot.ipynb

you may want to expose these notebooks to the internet so other people can use them to do this you need to 
1) set up an ssh k using '''ssh-keygen'''
2) run '''jupyter notebook --generate-config''' this will generate a config file at '''~/.jupyter'''
3) c.NotebookApp.allow_remote_access = True in that file
4) run '''ssh -R 80:localhost:<port of jupyter notebook> localhost.run'''  to run the app on the internet any user will need the token of the jupyter notebook to log in