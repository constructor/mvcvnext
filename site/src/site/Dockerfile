# Use Microsoft aspnet image as our base
FROM microsoft/aspnet:1.0.0-beta4

ADD . /app

# The COPY line tells Docker that we will copy contents of this folder (.) to # the /app directory of the container...
COPY . /app

# and the WORKDIR instruction will move us to the /app directory.
WORKDIR /app

# Restore packages with kpm
RUN ["dnu", "restore"]

# Exposes port 5004 to the world
EXPOSE 5004

# Configure the command to start the container
# In this instance we’re starting the Kestrel web server
ENTRYPOINT ["dnx", "project.json", "kestrel"]