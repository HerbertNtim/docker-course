# inherit from a existing image to add the functionality
FROM node:20-alpine3.18

# RUN addgroup app && adduser -S -G app app
# USER app

# Set the working directory and assign ownership to the non-root user
WORKDIR /app

# Copy the package.json and package-lock.json files into the image.
COPY package*.json ./

# change ownership of the /app directory to the app user
# USER root

# change ownership of the /app directory to the app user
# chown -R <user>:<group> <directory>
# chown command changes the user and/or group ownership of for given file.
# RUN chown -R app:app .

# change the user back to the app user
# USER app

# Install the dependencies.
RUN npm install

# Copy the rest of the source files into the image.
COPY . .

# Expose the port that the application listens on.
EXPOSE 3000

# Run the application.
CMD npm run dev