pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage ('Compile Stage') {
            // Get maven home path
            steps {
                    sh 'mvn clean package'          
            }   
        }        
    
        stage ('SonarQube analysis') {
            steps {
                // Optionally use a Maven environment you've configured already
                sh 'package sonar:sonar'
            }
        }
    }

}