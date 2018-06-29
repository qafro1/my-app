pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage ('Compile Stage') {
            // Get maven home path
            def mvnHome = tools name: 'maven',type: 'maven'
            steps {
                 sh "${mvnHome}/bin/mvn package"        
            }   
        }        
    }

}