# Use Microsoft aspnet image as our base
FROM microsoft/aspnet

# Copy the contents of /app/wwwroot to the /app directory of the container
COPY . /app

# Move to the /app directory of the container
WORKDIR /app

# Restore packages with kpm
RUN ["kpm", "restore"]

# Exposes port 5004 to the world
EXPOSE 5004

# Configure the command to start the container
# In this instance we’re starting the Kestrel web server
ENTRYPOINT ["k", "kestrel"]