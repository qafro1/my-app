pipeline {
    agent any
    stages {
        stage ('SCM') {
            steps {
                git 'https://github.com/qafro1/my-app.git'
            }
        }

    }
    
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