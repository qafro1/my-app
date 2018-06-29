pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage('build && SonarQube analysis') {
            steps {
                // Optionally use a Maven environment you've configured already
                withMaven(maven:'Maven') {
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }

}