# Use an official Node runtime as a parent image
FROM node:20

# Set the working directory in the container
WORKDIR /konga

# Clone the Git repository
RUN git clone https://github.com/pantsel/konga.git .

# Install dependencies
RUN npm install
RUN npm run bower-deps

# Make port 1337 available to the world outside this container
EXPOSE 1337

# Define environment variables
ENV NODE_ENV production

# Run the app when the container launches
CMD ["npm", "start"]