pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage('build && SonarQube analysis') {
            steps {
                // Optionally use a Maven environment you've configured already
                    sh 'mvn clean package sonar:sonar'
            }
        }
    }

}