pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage ('Compile Stage') {
            // Get maven home path
            steps {
                 sh "${mvnHome}/bin/mvn package"        
            }   
        }        
    
        stage ('SonarQube analysis') {
            steps {
                // Optionally use a Maven environment you've configured already
               
            }
        }
    }

}