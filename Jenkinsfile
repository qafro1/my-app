pipeline {
    agent any
    
    stages {
        stage ('Compile Stage') {
            // Get maven home path
            steps {
                
                    sh 'mvn clean package'
                
            }   
        }        
    }

}