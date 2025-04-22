# Jenkins Trigger Pipeline Demo

This repository demonstrates the use of different trigger mechanisms in Jenkins for automating job executions.

## Description

The `Jenkinsfile` included in this repository is a simple and functional pipeline designed to test and showcase three types of Jenkins triggers:

1. **GitHub Webhook Trigger**  
   Automatically triggers a build when a new push is made to the repository.

2. **Build Periodically Trigger**  
   Uses a CRON expression to schedule jobs at regular intervals.

3. **Poll SCM Trigger**  
   Periodically checks the Git repository for changes and triggers a build if any changes are detected.

This project is purely educational and aims to test and validate how Jenkins reacts to each trigger configuration.

## Jenkinsfile Overview

The pipeline contains a single stage:

```groovy
pipeline {
    agent any

    stages {
        stage('Trigger Test') {
            steps {
                echo 'Pipeline triggered successfully!'
            }
        }
    }
}
Tested With
Jenkins LTS

GitHub Webhook

CRON schedules for periodic builds

Polling for SCM changes

How to Use
Clone this repository.

Create a new pipeline job in Jenkins.

Set the job to use this repository's Jenkinsfile from SCM.

Test each trigger type:

Push to GitHub for webhook.

Set a CRON expression in "Build periodically".

Enable "Poll SCM" with a polling schedule.

Ensure webhook URL and GitHub credentials are properly configured in Jenkins.

 Notes
Make sure Jenkins has internet access and correct GitHub integration.

You can combine triggers or test them individually.

Keep the pipeline simple to focus on trigger behavior.

Screenshots 
Add screenshots here showing each trigger in action.