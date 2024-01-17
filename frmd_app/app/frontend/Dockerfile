# pull the latest official node image
FROM node:latest

# expose ports
EXPOSE 3000
EXPOSE 35729

# set working directory
WORKDIR /app

# add /app/node_modules/.bin to environment variables
ENV PATH /app/node_modules/.bin:$PATH

# copy package files and install app dependencies
COPY package.json /app/package.json
COPY package-lock.json /app/package-lock.json
RUN npm install
RUN npm install react-scripts -g

# add React app to working directory 
ADD . /app

# start the React app 
CMD ["npm", "start"]