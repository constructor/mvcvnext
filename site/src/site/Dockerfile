# Use Microsoft aspnet image as our base
FROM microsoft/aspnet:vs-1.0.0-beta4

ADD . /app

# The COPY line tells Docker that we will copy contents of this folder (.) to # the /app directory of the container...
COPY . /app

# and the WORKDIR instruction will move us to the /app directory.
WORKDIR /app

# Exposes port 5004 to the world
EXPOSE 5004

# Configure the command to start the container
ENTRYPOINT ["dnx", "./wwwroot", "kestrel"]