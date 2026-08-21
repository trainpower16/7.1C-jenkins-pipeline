pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {

        stage('Build') {
            steps {
                echo 'Stage 1: Build'
                echo 'Task: Compile the source code and package it into a deployable artifact such as a JAR or WAR file.'
                echo 'Tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Unit and Integration Tests'
                echo 'Task: Run unit tests to check each function on its own, then run integration tests to check that the components work together.'
                echo 'Tools: JUnit for unit tests, Selenium WebDriver for integration tests'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis'
                echo 'Task: Inspect the source code for code smells, duplication, complexity and style problems so it meets industry standards.'
                echo 'Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan'
                echo 'Task: Scan the source code and its third party dependencies for known vulnerabilities and report the CVEs found.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging'
                echo 'Task: Copy the packaged artifact to the staging server and start the application there.'
                echo 'Tool: AWS CLI deploying to an EC2 instance'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Integration Tests on Staging'
                echo 'Task: Run the integration test suite against the staging server to confirm the app behaves correctly in a production-like environment.'
                echo 'Tool: Selenium WebDriver'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production'
                echo 'Task: Release the approved build to the production server so real users can access it.'
                echo 'Tool: AWS CLI deploying to an EC2 instance'
            }
        }
    }
}
