# blue-green-docker
##Blue &amp; Green: Mini project #1

On the commandline run: `docker build -t flaskdock .`

The above docker build file uses the -t flag to tag the image with the name of flaskdock.

If the build worked successfully we can see the image in with the docker image ls command: `docker image ls`

You should then see your tag name in the images list:

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
flaskdock           latest              24045e0464af        2 minutes ago       165MB

The App is saved as `app.py`

The requirements.txt file within the same directory as app.py specifies our Flask dependency: `flask==1.0.2`


##Running the Container
Now that we have our image in hand along with the Python code in a file we can run the image as a container with the docker run command. Execute the following command, making sure to replace the absolute path for the volume to your own directory.

docker run -p 5000:80 --volume=/Users/amira/desktop/py/flaskdocker:/app flaskdock
If you receive the error python: can't open file 'app.py': [Errno 2] No such file or directory then you likely forgot to change /Users/amira/desktop/py/flaskdocker to the directory where the project files are located.
