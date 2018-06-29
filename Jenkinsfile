pipeline {
    agent any
    
    stages {
        stage ('Compile Stage') {
            // Get maven home path
            steps {
                withMaven(maven:'maven'){
                    sh 'mvn clean package'
                }
            }   
        }        
    }

}