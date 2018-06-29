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
    }

}