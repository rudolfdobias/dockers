# Change to alpine linux when possible
FROM microsoft/dotnet:1.1.0-sdk-projectjson

RUN wget -qO- https://deb.nodesource.com/setup_7.x | bash -
RUN apt-get install -y libfontconfig bzip2 nodejs
RUN npm install -g firefly-pdf-render