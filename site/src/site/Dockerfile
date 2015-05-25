FROM microsoft/aspnet:vs-1.0.0-beta4

ADD . /app

WORKDIR /app

EXPOSE 5001

ENTRYPOINT ["dnx", ".", "Kestrel"]