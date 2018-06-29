pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage('build ') {
            steps {
                // Optionally use a Maven environment you've configured already
                    sh 'mvn clean package'
            }
        }
    }

}