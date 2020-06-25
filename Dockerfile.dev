# Use an existing docker image as base
FROM node:alpine 

# So the folders files copied on the next command are pasted on the specified directory (/usr/app)
WORKDIR "/app"

# Download and install dependency. To run the npm install command, we only need the 'package.json' file.
COPY ./package.json ./
RUN npm install

# The .. means that everything from the frontend directory will be copied into the image.
# This way, we don't have to run the RUN npm install command each time that we change our files (f.e.: index.js).
COPY . .

# Tell the image what to do when it start as a container 	
CMD ["npm", "run", "start"]