pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage ('Compile Stage') {
            // Get maven home path
            steps {
                 def mvnHome =  tool name: 'maven', type: 'maven' 
                 sh "${mvnHome}/bin/mvn package"        
            }   
        }        
    }

}