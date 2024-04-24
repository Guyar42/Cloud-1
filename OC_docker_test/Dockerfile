FROM openclassrooms/build_image

RUN apt-get update \
&& apt-get upgrade -y \
&& apt-get install nginx -y

# FROM nginx:latest

# CMD ["echo", "Hello World!"]
##################################################

# FROM debian:latest

# Installation de nodejs
# RUN apt-get update -yq
# RUN apt-get install curl gnupg -yq
# RUN apt-get install nodejs -yq 
# RUN apt-get clean -y

# #copie le contenu du répertoire courant dans le répertoire /app du container
# ADD . /app/

# #workdir est l'équivalent de cd, il exécute toutes les commandes dans le répertoire /app
# WORKDIR /app

# # RUN npm install

# EXPOSE 2368

# VOLUME /app/logs

# CMD npm run start