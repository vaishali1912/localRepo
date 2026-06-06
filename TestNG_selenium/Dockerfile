# Use Maven image with JDK 21
FROM maven:3.9.14-eclipse-temurin-17

# Set working directory inside the container
WORKDIR /app

# Copy the project files to the container
COPY . .

# Download dependencies and build the project (skip tests for build speed)
RUN mvn clean install -DskipTests

# Run TestNG tests when the container starts
# Replace "testng.xml" with your TestNG suite file name if different
CMD ["mvn", "test", "-DsuiteXmlFile=testng.xml"]
