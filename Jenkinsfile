pipeline {
    agent any
    tools {
        maven 'maven'
    }
    
    stages {
        stage('build && SonarQube analysis') {
            steps {
                withSonarQubeEnv('sonar') {
                    // Optionally use a Maven environment you've configured already
                    sh 'mvn clean package sonar:sonar'
                }
            }
        }
    }
        stage ('Quality Gate') {
            steps {
                withSonarQubeEnv('sonar') {
                    sh 'mvn clean package sonar:sonar'
                    timeout(time: 1, unit: 'HOURS') {
                    // Parameter indicates whether to set pipeline to UNSTABLE if Quality Gate fails
                    // true = set pipeline to UNSTABLE, false = don't
                    // Requires SonarQube Scanner for Jenkins 2.7+
                    waitForQualityGate abortPipeline: true
                 }
                }
            }

        }

}