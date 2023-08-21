# jenkins-ex
example plugin


reating a simple "Hello, World!" Jenkins plugin involves several steps. Below is a step-by-step guide to create a Jenkins plugin using Maven, as it's the most commonly used build tool for Jenkins plugins.

# Prerequisites
Java Development Kit (JDK): Install JDK 8 or above.
Maven: Install Maven 3.x.
Jenkins: Install Jenkins for testing the plugin.
IDE: Install an IDE like IntelliJ IDEA or Eclipse.

## Step 1: Generate Plugin Template
Open a terminal and run the following command to generate a Maven archetype for a Jenkins plugin:

```
mvn archetype:generate -Dfilter=io.jenkins.archetypes:
```
Follow the prompts to set up your plugin. Choose the "hello-world" archetype if available.

## Step 2: Import Project into IDE
Import the generated Maven project into your IDE.

## Step 3: Examine the Code
The generated code should include a class that extends hudson.model.BuildStep. This class will contain a perform method, which is where you can add your "Hello, World!" logic.

## Step 4: Modify the perform Method
Open the main class and locate the perform method. Add a line to print "Hello, World!" to the build log:

```
listener.getLogger().println("Hello, World!");
```


## Step 5: Build the Plugin
In the terminal, navigate to your project directory and run:

bash
Copy code
mvn package
This will create a .hpi file in the target directory.

## Step 6: Install and Test the Plugin
Open your Jenkins instance and navigate to Manage Jenkins > Manage Plugins > Advanced.
Upload the .hpi file and restart Jenkins.
Create a new freestyle project and add your "Hello, World!" build step.
Run the build and check the console output for the "Hello, World!" message.

## Step 7: Further Steps
You can now continue to develop more complex features, write tests, and eventually publish your plugin to the Jenkins Plugin Repository.

